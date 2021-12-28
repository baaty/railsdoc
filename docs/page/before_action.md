---
layout: page
---

### 説明

アクションの前に処理を実行

### 使い方

    before_action(アクション名, only: 実行するアクション=nil, except: 実行しないアクション=nil, if: 実行する条件を指定=nil, unless: 実行されない条件を指定=nil, ブロック)

### 例

#### アクションの前に処理を実行

    before_action :require_permission
    def require_permission
      unless current_user.partner? || current_user.admin?
        redirect_to admin_root_path, alert: 'ここから先は管理者限定です！'
      end
    end

#### 実行するアクションを指定

    before_action :render_form, only: [:new :edit]
    def render_form
      render 'form'
    end

#### 複数指定

    before_action :user1
    before_action :user2

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/abstract_controller/callbacks.rb#L106)

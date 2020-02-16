---
layout: page
---
### 説明
アクションの前に処理を実行

### 使い方
    before_action(アクション名 [, オプション])

### オプション

オプション   | 説明
--------|------------
:only   | 実行するアクション
:except | 実行しないアクション
:if     | 実行する条件を指定
:unless | 実行されない条件を指定

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/callbacks.rb#L111)
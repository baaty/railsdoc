---
layout: archive_page
---
### 説明
アクションの後に処理を実行

### 使い方
    after_action(アクション名 [, オプション])

### オプション

オプション   | 説明
--------|------------
:only   | 実行するアクション
:except | 実行しないアクション
:if     | 実行する条件を指定
:unless | 実行されない条件を指定

### 例
#### アクションの後に処理を実行
    after_action :store_location
    def store_location
      if request.fullpath !~ Regexp.new('\\A/users/.*\\z') && !request.xhr?
        session[:previous_url] = request.fullpath
      end
    end

#### 実行するアクションを指定
    after_action :render_form, only: [:new :edit]
    def render_form
      render 'form'
    end

#### 複数指定
    before_action :user1
    before_action :user2

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/abstract_controller/callbacks.rb#L135)
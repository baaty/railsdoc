---
layout: page
---
### 説明
アクションの前に処理を実行

### 使い方
    before_action 名前 [, only: アクション名]

### 例
    before_action :login
    def login
      redirect_to login_url unless signed_in?
    end


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/callbacks.rb#L111)
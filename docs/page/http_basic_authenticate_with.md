---
layout: page
---
### 説明
Basic認証

### 使い方
    http_basic_authenticate_with(name: 名前, password: パスワード [, realm: 認証が必要がエリア名, オプション])

### 例
#### Basic認証
    http_basic_authenticate_with name: ENV['BASIC_AUTH_USERNAME'], password: ENV['BASIC_AUTH_PASSWORD'] if Rails.env == 'staging'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/http_authentication.rb#L72)
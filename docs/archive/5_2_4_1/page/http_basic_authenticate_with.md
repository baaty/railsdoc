---
layout: archive_page
---
### 説明
Basic認証

### 使い方
    http_basic_authenticate_with(name: 名前, password: パスワード [, realm: 認証が必要がエリア名, オプション])

### 例
#### Basic認証
    http_basic_authenticate_with name: ENV['BASIC_AUTH_USERNAME'], password: ENV['BASIC_AUTH_PASSWORD'] if Rails.env == 'staging'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_controller/metal/http_authentication.rb#L71)
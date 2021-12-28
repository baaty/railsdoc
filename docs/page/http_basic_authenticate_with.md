---
layout: page
---

### 説明

Basic認証

### 使い方

    http_basic_authenticate_with(name: 名前, password: パスワード, realm: 認証が必要がエリア名=nil, オプション引数)

### 例

    http_basic_authenticate_with name: ENV['BASIC_AUTH_USERNAME'], password: ENV['BASIC_AUTH_PASSWORD'] if Rails.env == 'staging'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/http_authentication.rb#L73)

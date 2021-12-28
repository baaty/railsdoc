---
layout: page
---

### 説明

CSRF対策の設定

### 使い方

    protect_from_forgery(オプション={})

### オプション

| オプション | 説明                   |
| ---------- | ---------------------- |
| :only      | 実行するアクション     |
| :except    | 実行しないアクション   |
| :if        | 実行する条件を指定     |
| :unless    | 実行されない条件を指定 |
| :prepend   |                        |
| :with      |                        |

### 例

#### CSRF対策の設定

    protect_from_forgery except: :index

#### CSRF対策の設定

    protect_from_forgery with: :exception

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/request_forgery_protection.rb#L156)

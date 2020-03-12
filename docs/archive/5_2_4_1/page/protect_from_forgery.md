---
layout: archive_page
---
### 説明
CSRF対策の設定

### 使い方
    protect_from_forgery([オプション])

### オプション

オプション    | 説明
---------|------------
:only    | 実行するアクション
:except  | 実行しないアクション
:if      | 実行する条件を指定
:unless  | 実行されない条件を指定
:prepend |
:with    |

### 例
#### CSRF対策の設定
    protect_from_forgery except: :index

#### CSRF対策の設定
    protect_from_forgery with: :exception

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/request_forgery_protection.rb#L135)
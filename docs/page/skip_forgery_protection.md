---
layout: page
---

### 説明

CSRF対策の設定をオフ

### 使い方

    skip_forgery_protection(オプション={})

### オプション

| 名前           | 説明                                           |
| -------------- | ---------------------------------------------- |
| :only/:except  | 偽造防止機能をアクションのサブセットにのみ適用 |
| :if/:unless    | 条件に応じて偽装防止機能を完全にオフ           |
| :prepend       | 事前に実行                                     |
| :with          | 検証されていないリクエストを処理する方法       |
| :exception     | 例外を発生                                     |
| :reset_session | セッションをリセット                           |
| :null_session  | リクエスト時に空のセッション                   |

### 例

    skip_before_action :verify_authenticity_token

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/request_forgery_protection.rb#L170)

---
layout: page
---

### 説明

アクションの実行前にチェック

### 使い方

    verify(引数.., オプション引数)

### オプション

| オプション   | 説明                                       |
| ------------ | ------------------------------------------ |
| :params      | パラメータがあるか                         |
| :session     | セッションにキーがあるか                   |
| :flash       | フラッシュの中に指摘したキーのデータあるか |
| :method      | HTTPのメソッドが指定したものか             |
| :xhr         | アクションがAjaxから呼ばれたか             |
| :add_flash   | フラッシュにデータを追加                   |
| :add_headers | HTTPのヘッダに「カラム名:値」を追加        |
| :redirect_to | 別のアクションにリダイレクト               |
| :render      | 別のアクションのテンプレートでレンダリング |
| :only        | 適用するアクション                         |
| :except      | 適応しないアクション                       |

### 例

#### セッションにuser_idがない場合は、indexにリダイレクト

    verify session: "user_id", redirect_to: { action: "index" }

#### POSTでアクセスしていない場合は、indexにリダイレクト

    verify method: :post, redirect_to: { action: "index" }

#### create, update, deleteアクション以外は、indexにリダイレクト

    verify only: [:create, :update, :delete], :redirect_to { action: "index" }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/message_verifier.rb#L177)

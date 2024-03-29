---
layout: page
---

### 説明

URLを指定して表示

### 使い方

    redirect_to(オプション={}, レスポンスオプション={})

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :alert     | エラーメッセージを表示               |
| :notice    | 通知用のメッセージを表示             |
| :flash     | パラメータを使って、一時的に値を保存 |

### ステータスコード

| シンボル               | コード | 説明                           |
| ---------------------- | ------ | ------------------------------ |
| :ok                    | 200    | 成功                           |
| :created               | 201    | リソースの生成に成功           |
| :moved_permanently     | 301    | リソースが永続的にリダイレクト |
| :found                 | 302    | リソースが一時的にリダイレクト |
| :see_other             | 303    | リソースが別の場所にある       |
| :bad_request           | 400    | 不正なリクエスト               |
| :unauthorized          | 401    | 未承認                         |
| :forbidden             | 403    | アクセス禁止                   |
| :not_found             | 404    | リソースが存在しない           |
| :method_not_allowed    | 405    | HTMLメソッドが許可されていない |
| :internal_server_error | 500    | 内部サーバエラー               |

### 例

#### 指定したページにリダイレクト

    redirect_to action: "show", id: 5

#### インスタンス変数

    redirect_to @post

#### URL

    redirect_to "http://www.rubyonrails.org"

#### ステータスコード指定

    redirect_to post_url(@post), status: 301

#### エラーメッセージを表示

    redirect_to post_url(@post), alert: "Watch it, mister!"

#### 通知メッセージを表示

    redirect_to post_url(@post), status: :found, notice: "Pay attention to the road"

#### flash指定

    redirect_to post_url(@post), status: 301, flash: { updated_post_id: @post.id }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/redirecting.rb#L82)

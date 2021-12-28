---
layout: page
---
### 説明
URLを指定して表示

### 使い方
    redirect_to(リダイレクト先のパス [, status: ステイタスコード, オプション])

### ステータスコード

シンボル                 | コード | 説明
---------------------- | --- | -----------------
:ok                    | 200 | 成功
:created               | 201 | リソースの生成に成功
:moved_permanently     | 301 | リソースが永続的にリダイレクト
:found                 | 302 | リソースが一時的にリダイレクト
:see_other             | 303 | リソースが別の場所にある
:bad_request           | 400 | 不正なリクエスト
:unauthorized          | 401 | 未承認
:forbidden             | 403 | アクセス禁止
:not_found             | 404 | リソースが存在しない
:method_not_allowed    | 405 | HTMLメソッドが許可されていない
:internal_server_error | 500 | 内部サーバエラー

### オプション

オプション      | 説明
------------- | ------------------
:alert        | エラーメッセージを表示
:notice       | 通知用のメッセージを表示
:flash        | パラメータを使って、一時的に値を保存

### 例
#### 指定したページにリダイレクト
    redirect_to action: "show", id: 5

#### インスタンス変数
    redirect_to @post

#### URL
    redirect_to "http://www.rubyonrails.org"

#### 相対パス
    redirect_to "/images/screenshot.jpg"

#### ステータスコード指定
    redirect_to post_url(@post), status: 301

#### エラ〜メッセージを表示
    redirect_to post_url(@post), alert: "Watch it, mister!"

#### 通知メッセージを表示
    redirect_to post_url(@post), status: :found, notice: "Pay attention to the road"

#### flash指定
    redirect_to post_url(@post), status: 301, flash: { updated_post_id: @post.id }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/redirecting.rb#L58)
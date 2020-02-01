---
layout: page
---
### 説明
応答ステータスとヘッダ情報のみを表示

### 使い方
    head(ステータスコード [, 応答ヘッダ])

### ステータスコード

シンボル                   | コード | 説明
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

### 例
#### 応答ステータスとヘッダ情報のみを表示
    head :created, location: person_path(@person)

#### ステータスコード200
    head :ok

#### ステータスコード404
    head :not_found

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/head.rb#L21)
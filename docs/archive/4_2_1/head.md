---
layout: page
---
### 説明
応答ステータスとヘッダ情報のみを表示

### 使い方
    head ステータスコード [, 応答ヘッダ]

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
#### 404 Not Foundを返す
    head :not_found

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/97a17dc7343b68aaf73d6af4a2bb205141e22d9b/actionpack/lib/action_controller/metal/head.rb#L19)
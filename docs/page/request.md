---
layout: page
---
### 説明
リクエストを送ってきたユーザのヘッダー情報や環境変数を取得

### 使い方
    request.メソッド

### メソッド

メソッド名                    | 説明
--------------------------|---------------------
GET                       |
POST                      |
accept_encoding           | エンコーディング形式を取得
accept_language           | 受信可能な言語
authority                 | authorityを取得
authorization             | 認証情報を取得
base_url                  | URLを取得
body                      | ポストデータを取得
content_charset           | charsetパラメータを取得
content_length            | コンテンツサイズを取得
content_type              | content-typeを取得
controller_class          |
controller_class_for      |
cookie_jar                |
cookies                   | クッキーを取得
delete?                   | HTTPメソッドがDELETEであるか？
get?                      | HTTPメソッドがGETであるか？
head?                     | HTTPメソッドがHEADであるか？
host                      | ホスト名を取得
host_with_port            | ホスト名とポート番号を取得
form_data?                | フォームデータがあるか？
fullpath                  | リクエストURLを取得
headers                   | リクエストヘッダーの情報取得
http_auth_salt            |
ip                        | IPアドレスを取得
link?                     | HTTPメソッドがLINKであるか？
key?                      | 一致するヘッダーがあるか？
local?                    | ローカル通信であるか
logger                    |
media_type                | メディア対応の取得
media_type_params         |
method                    | HTTPメソッド
method_symbol             | メソッドをシンボルで取得
multithread?              |
new                       |
original_fullpath         | 最後に要求されたパスを取得
original_url              | 元のリクエストURLを取得
options?                  |
parseable_data?           |
patch?                    | HTTPメソッドがPATCHであるか？
path                      |
path_info                 |
path_info=                |
port                      | ポート番号
post?                     | HTTPメソッドがPOSTであるか？
put?                      | HTTPメソッドがPUTであるか？
query_string              | クエリ文字(?より後ろの部分)
referer                   |
query_parameters          |
raw_post                  | リクエスト本文を取得
remote_ip                 | クライアントのipアドレスを取得
request_id                | X-Request-Idヘッダーを取得
request_method            | リクエストメソッドを取得
request_method_symbol     | リクエストメソッドをシンボルで取得
request_parameters        |
reset_session             |
scheme                    |
script_name               |
script_name=              |
session                   |
session_options           |
send_early_hints          |
server_software           | 使用しているサーバソフトウェア
session_options=(options) |
ssl?                      |
trace?                    |
trusted_proxy?            |
unlink?                   |
url                       | リクエストのURLを取得
user_agent                | ユーザエージェントを取得
values_at                 |
uuid                      | X-Request-Idヘッダーを取得
xhr?                      | 「X-Requested-With」ヘッダーに「XMLHttpRequest」が含まれているか？
xml_http_request?         | Ajaxによって実行されたものか

### 例
#### リクエストメソッドの取得
    request.request_method

#### リンク先のURLを取得
    request.headers[:referer]

#### すべてのリクエストヘッダを取得
    request.headers

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/http/request.rb)
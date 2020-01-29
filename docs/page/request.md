---
layout: page
---
### 説明
リクエストを送ってきたユーザのヘッダー情報や環境変数を取得

### 使い方
    request.メソッド

### メソッド

メソッド名                  | 説明
------------------------- | -----------------------------------------------
GET                       |
POST                      |
authorization             | 認証情報を取得
body                      | ポストデータを取得
commit_flash              |
content_length            | コンテンツサイズを取得
content_class             |
controller_class          |
controller_class_for      |
cookie_jar                |
empty                     |
form_data?                |
fullpath                  | リクエストURLを取得
headers                   | リクエストヘッダーの情報取得
http_auth_salt            |
ip                        | IPアドレスを取得
key?                      |
local?                    | ローカル通信であるか
logger                    |
media_type                | メディア対応の取得
method                    | HEAD以外は、「request.request_method」と同じ。headはgetを取得
method_symbol             | メソッドをシンボルで取得
new                       |
original_fullpath         |
original_url              |
query_parameters          |
raw_post                  |
remote_ip                 | remote_ipを取得
request_method            | リクエストメソッドを取得
request_method_symbol     | リクエストメソッドをシンボルで取得
request_parameters        |
reset_session             |
send_early_hints          |
server_software           | 使用しているサーバソフトウェアを取得
session_options=(options) |
ssl?                      |
uuid                      |
xhr?                      |
xml_http_request?         | Ajaxによって実行されたものかどうか

### 例
#### リクエストメソッドの取得
    request.request_method

#### リンク先のURLを取得
    request.headers[:referer]

#### すべてのリクエストヘッダを取得
    request.headers

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/http/request.rb)
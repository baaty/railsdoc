---
layout: page
---
### 説明
リクエストを送ってきたユーザのヘッダー情報や環境変数を取得

### 使い方
    request.メソッド

### メソッド

メソッド名                     | 説明
------------------------- | -----------------------------------------------
request_method            | リクエストメソッドを取得
request_method_symbol     | リクエストメソッドをシンボルで取得
method                    | HEAD以外は、「request.request_method」と同じ。headはgetを取得
method_symbol             | メソッドをシンボルで取得
get?                      | GET かどうか
post?                     | POSTかどうか
patch?                    | PATCHかどうか
put?                      | PUTかどうか
delete?                   | DELETEかどうか
head?                     | HEADかどうか
headers                   | リクエストヘッダーの情報取得
original_fullpath         |
fullpath                  | リクエストURLを取得
original_url              |
media_type                | メディア対応の取得
content_length            | コンテンツサイズを取得
xml_http_request?         | Ajaxによって実行されたものかどうか
ip                        | IPアドレスを取得
remote_ip                 | remote_ipを取得
uuid                      |
server_software           | 使用しているサーバソフトウェアを取得
raw_post                  |
body                      | ポストデータを取得
form_data?                |
body_stream               |
reset_session             |
session=(session)         |
session_options=(options) |
authorization             | 認証情報を取得
local?                    | ローカル通信であるか
deep_munge                | paramsからnilを削除

### 例
#### リクエストメソッドの取得
    request.request_method

#### リンク先のURLを取得
    request.headers[:referer]

#### すべてのリクエストヘッダを取得
    request.headers
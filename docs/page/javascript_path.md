---
layout: page
---
### 説明
JavaScriptファイルへのパスを取得

### 使い方
    javascript_path(ファイルへのパス [, オプション])

### オプション

オプション      | 説明
---------- | -------------
:extname   | 拡張子がない場合に拡張子を追加
:protocol | プロトコルを指定
:host     | 相対パスの場合にホストを追加
:skip_pipeline | アセットパイプラインをスキップ
:nonce |

### 例
#### JavaScriptファイルへのパスを生成
    <%= javascript_path "example" %>
    # /javascripts/example.js

#### サブディレクトリにあるJavaScriptファイルへのパスを生成
    <%= javascript_path "dir/example.js" %>
    # /javascripts/dir/example.js

#### JavaScriptファイルへのパスを絶対パスで指定して生成
    <%= javascript_path "/dir/example" %>
    # /dir/example.js %>

#### 外部サイトにあるJavaScriptファイルへのパスを生成
    <%= javascript_path "http://www.example.com/js/example" %>
    # http://www.example.com/js/example

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L318)
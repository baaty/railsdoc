---
layout: page
---
### 説明
JavaScriptファイルへのパスを取得

### 使い方
    javascript_path(ファイルへのパス [, オプション])

### オプション

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
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L244)
---
layout: archive_page
---
### 説明
JavaScriptファイルへのURLを取得

### 使い方
    javascript_url(ファイルへのパス [, オプション])

### オプション

オプション          | 説明
---------------|----------------
:host          | 相対パスの場合にホストを追加

### 例
    javascript_url "js/xmlhr.js", host: "http://stage.example.com"
    # http://stage.example.com/assets/js/xmlhr.js


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_url_helper.rb#L329)
---
layout: page
---
### 説明
外部スタイルシートへのURLを生成

### 使い方
    stylesheet_url(ファイルへのパス [, オプション])

### オプション

オプション          | 説明
---------------|----------------
:host          | 相対パスの場合にホストを追加

### 例
    stylesheet_url "css/style.css", host: "http://stage.example.com"
    # http://stage.example.com/assets/css/style.css


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L357)
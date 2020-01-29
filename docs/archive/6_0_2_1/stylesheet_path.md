---
layout: page
---
### 説明
スタイルシートへのパスを生成

### 使い方
    stylesheet_path(ファイルへのパス [, オプション])

### オプション

### 例
    stylesheet_path "style"
    # /stylesheets/style.css

    stylesheet_path "dir/style.css"
    # /stylesheets/dir/style.css

    stylesheet_path "/dir/style.css"
    # /dir/style.css

    stylesheet_path "http://www.example.com/css/style"
    # http://www.example.com/css/style

    stylesheet_path "http://www.example.com/css/style.css"
    # http://www.example.com/css/style.css

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L345)
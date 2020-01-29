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
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L266)
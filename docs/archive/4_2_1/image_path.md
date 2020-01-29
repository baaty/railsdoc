---
layout: page
---
### 説明
画像へのパスを取得

### 使い方
    image_path(ファイルへのパス [, オプション])

### オプション

### 例
#### 画像ファイルへのパスを生成
    image_path("example.png")
    # => "/images/example.png"

#### サブディレクトリにある画像ファイルへのパスを生成
    image_path("icons/example.png")
    # => "/images/icons/example.png"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L291)
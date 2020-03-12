---
layout: archive_page
---
### 説明
画像へのパスを取得

### 使い方
    image_path(ファイルへのパス [, オプション])

### オプション

オプション | 説明
----- | --------
:type | ファイルのタイプ

### 例
#### 画像ファイルへのパスを生成
    image_path("example.png")
    # "/images/example.png"

#### サブディレクトリにある画像ファイルへのパスを生成
    image_path("icons/example.png")
    # "/images/icons/example.png"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_url_helper.rb#L374)
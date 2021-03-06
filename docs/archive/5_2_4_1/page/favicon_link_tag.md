---
layout: archive_page
---
### 説明
ファビコンのタグを生成

### 使い方
    favicon_link_tag(画像へのパス [, オプション])

### オプション

オプション  | 説明
-------|----------------
:rel   | 外部文章との関係
:type  | コンテンツタイプ
:sizes | サイズ

### 例
#### ファビコンを表示するタグを生成
    favicon_link_tag
    # <link href="/assets/favicon.ico" rel="shortcut icon" type="image/x-icon" />

#### ファビコン名を指定してタグを生成
    favicon_link_tag 'myicon.ico'
    # <link href="/assets/myicon.ico" rel="shortcut icon" type="image/x-icon" />

#### サイズ指定
    favicon_link_tag 'favicons/fav-16x16.png', type: 'image/png', sizes: "16x16"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_tag_helper.rb#L226)
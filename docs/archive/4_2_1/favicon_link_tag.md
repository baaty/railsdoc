---
layout: page
---
### 説明
ファビコンを設定

### 使い方
    favicon_link_tag(画像へのパス [, オプション])

### オプション

オプション  | 説明       | デフォルト
------ | -------- | -------------------
:rel   | 外部文章との関係 | alternate
:type  | コンテンツタイプ | application/rss+xml
:title | タイトル     | RSS

### 例
#### ファビコンを表示するタグを生成
    <%= favicon_link_tag 'favicon.ico' %>
    # <link href="/images/favicon.ico" rel="shortcut icon" type="image/vnd.microsoft.icon" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L172)
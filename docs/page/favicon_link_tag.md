---
layout: page
---

### 説明

ファビコンのタグを生成

### 使い方

    favicon_link_tag(画像へのパス='favicon.ico', オプション={})

### オプション

| オプション | 説明             |
| ---------- | ---------------- |
| :rel       | 外部文章との関係 |
| :type      | コンテンツタイプ |
| :sizes     | サイズ           |

### 例

#### ファビコンを表示するタグを生成

    favicon_link_tag
    #=> <link href="/assets/favicon.ico" rel="shortcut icon" type="image/x-icon" />

#### ファビコン名を指定してタグを生成

    favicon_link_tag 'myicon.ico'
    #=> <link href="/assets/myicon.ico" rel="shortcut icon" type="image/x-icon" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_tag_helper.rb#L276)

---
layout: page
---

### 説明

フォントアセットへの絶対パス

### 使い方

    font_url(フォントファイルへのパス, オプション={})

### オプション

| オプション     | 説明                         |
| -------------- | ---------------------------- |
| :type          | ファイルのタイプ             |
| :skip_pipeline | assetsのpathを付けない       |
| :extname       | 拡張子指定                   |
| :host          | 相対パスの場合にホストを追加 |
| :protocol      | プロトコル                   |

### 例

#### フォントアセットへの絶対パス

    font_url "font.ttf"

#### host指定

    font_url "font.ttf", host: "http://stage.example.com"
    #=> http://stage.example.com/fonts/font.ttf

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_url_helper.rb#L466)

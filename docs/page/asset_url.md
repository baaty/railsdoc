---
layout: page
---

### 説明

公開ディレクトリにあるアセットへの絶対パス

### 使い方

    asset_url(ファイルへのパス, オプション={})

### オプション

| オプション     | 説明                         |
| -------------- | ---------------------------- |
| :type          | ファイルのタイプ             |
| :skip_pipeline | assetsのpathを付けない       |
| :extname       | 拡張子指定                   |
| :host          | 相対パスの場合にホストを追加 |
| :protocol      | プロトコル                   |

### 例

#### assetファイルへのパスを取得

    asset_url "application.js"
    #=> http://example.com/assets/application.js

#### hostを指定

    asset_url "application.js", host: "http://cdn.example.com"
    #=> http://cdn.example.com/assets/application.js

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_url_helper.rb#L230)

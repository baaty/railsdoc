---
layout: page
---

### 説明

公開されているaudiosディレクトリ内のオーディオアセットへの絶対パス

### 使い方

    audio_url(音声ファイルへのパス, オプション={})

### オプション

| オプション     | 説明                         |
| -------------- | ---------------------------- |
| :type          | ファイルのタイプ             |
| :skip_pipeline | assetsのpathを付けない       |
| :extname       | 拡張子指定                   |
| :host          | 相対パスの場合にホストを追加 |
| :protocol      | プロトコル                   |

### 例

#### オーディオアセットへの絶対パス

    audio_url "horse.wav"

#### hosts指定

    audio_url "horse.wav", host: "http://stage.example.com"
    #=> http://stage.example.com/audios/horse.wav

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_url_helper.rb#L441)

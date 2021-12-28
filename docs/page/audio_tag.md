---
layout: page
---

### 説明

モデルと関連のないHTML5で追加されたaudioを生成

### 使い方

    audio_tag(音声ファイルへのパス..)

### オプション

| オプション | 説明                     |
| ---------- | ------------------------ |
| :autoplay  | 自動再生を有効           |
| :controls  | コントローラパネルを表示 |
| :loop      | 繰り返し再生             |

### 例

#### audioを生成

    audio_tag("sound")
    #=> <audio src="/audios/sound" />

#### audioタグを生成して、自動再生を有効にして、コントローラパネルを表示

    audio_tag("sound.wav", autoplay: true, controls: true)
    #=> <audio autoplay="autoplay" controls="controls" src="/audios/sound.wav" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/asset_tag_helper.rb#L485)

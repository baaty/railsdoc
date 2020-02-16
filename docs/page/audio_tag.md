---
layout: page
---
### 説明
モデルと関連のないHTML5で追加されたaudioを生成

### 使い方
    audio_tag(音声ファイルへのパス, [オプション])

### オプション

| オプション     | 説明           |
|-----------|--------------|
| :autoplay | 自動再生を有効  |
| :controls | コントローラパネルを表示 |
| :loop     | 繰り返し再生     |

### 例
#### 基本形(オプションなし)
    audio_tag("sound")
    # <audio src="/audios/sound" />

#### audioタグを生成して、自動再生を有効にして、コントローラパネルを表示
    audio_tag("sound.wav", autoplay: true, controls: true)
    # <audio autoplay="autoplay" controls="controls" src="/audios/sound.wav" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_tag_helper.rb#L428)
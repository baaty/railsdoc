---
layout: page
---
### 説明
音声ファイルへのパスを取得

### 使い方
    audio_path(音声ファイルへのパス)

### 例
    audio_path("horse")
    # /audios/horse

    audio_path("horse.wav")
    # /audios/horse.wav

    audio_path("sounds/horse.wav")
    # /audios/sounds/horse.wav

    audio_path("/sounds/horse.wav")
    # /sounds/horse.wav

    audio_path("http://www.example.com/sounds/horse.wav")
    # http://www.example.com/sounds/horse.wav

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L333)
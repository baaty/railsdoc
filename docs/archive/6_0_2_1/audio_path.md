---
layout: page
---
### 説明
音声ファイルへのパスを取得

### 使い方
    audio_path(音声ファイルへのパス [, オプション])

### オプション

オプション | 説明
----- | --------
:type | ファイルのタイプ
:skip_pipeline | assetsのpathを付けない
:extname | 拡張子指定

### 例
#### 音声ファイルへのパスを取得
    audio_path("horse")
    # /audios/horse

#### 拡張子指定
    audio_path("horse.wav")
    # /audios/horse.wav

#### 相対パス
    audio_path("sounds/horse.wav")
    # /audios/sounds/horse.wav

#### 絶対パス
    audio_path("/sounds/horse.wav")
    # /sounds/horse.wav

#### URL指定
    audio_path("http://www.example.com/sounds/horse.wav")
    # http://www.example.com/sounds/horse.wav

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L427)
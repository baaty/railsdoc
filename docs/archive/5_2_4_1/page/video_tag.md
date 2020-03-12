---
layout: archive_page
---
### 説明
HTML5で追加されたvideoタグを生成

### 使い方
    video_tag(動画ファイルへのパス, [, オプション])

### オプション

オプション                 | 説明
----------------------|----------------
:poster               | サムネイル画像
:poster_skip_pipeline | アセットディレクトリを使わない
:autoplay             | 自動再生を有効
:controls             | コントローラパネルを表示
:loop                 | 繰り返し再生
:autobuffer           | 自動でバッファリング
:size                 | 動画サイズ(幅x高さ)
:width                | 動画の幅
:height               | 動画の高さ
:poster               | サムネイルを表示

### 例
#### HTML5で追加されたvideoタグを生成
    video_tag("trailer")
    # <video src="/videos/trailer"></video>

#### 拡張子まで指定
    video_tag("trailer.ogg")
    # <video src="/videos/trailer.ogg"></video>

#### パラメータを指定
    video_tag("trailer.ogg", controls: true, preload: 'none')
    # <video preload="none" controls="controls" src="/videos/trailer.ogg"></video>

#### サイズを指定
    video_tag("trailer.m4v", size: "16x10", poster: "screenshot.png")
    # <video src="/videos/trailer.m4v" width="16" height="10" poster="/assets/screenshot.png"></video>

#### 複数指定
    video_tag("trailer.ogg", "trailer.flv")
    # <video><source src="/videos/trailer.ogg" /><source src="/videos/trailer.flv" /></video>

#### 配列で指定
    video_tag(["trailer.ogg", "trailer.flv"])
    # <video><source src="/videos/trailer.ogg" /><source src="/videos/trailer.flv" /></video>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_tag_helper.rb#L424)
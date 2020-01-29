---
layout: page
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
    video_tag("trailer")
    # <video src="/videos/trailer"></video>

    video_tag("trailer.ogg")
    # <video src="/videos/trailer.ogg"></video>

    video_tag("trailer.ogg", controls: true, preload: 'none')
    # <video preload="none" controls="controls" src="/videos/trailer.ogg"></video>

    video_tag("trailer.m4v", size: "16x10", poster: "screenshot.png")
    # <video src="/videos/trailer.m4v" width="16" height="10" poster="/assets/screenshot.png"></video>

    video_tag("trailer.m4v", size: "16x10", poster: "screenshot.png", poster_skip_pipeline: true)
    # <video src="/videos/trailer.m4v" width="16" height="10" poster="screenshot.png"></video>

    video_tag("/trailers/hd.avi", size: "16x16")
    # <video src="/trailers/hd.avi" width="16" height="16"></video>

    video_tag("/trailers/hd.avi", size: "16")
    # <video height="16" src="/trailers/hd.avi" width="16"></video>

    video_tag("/trailers/hd.avi", height: '32', width: '32')
    # <video height="32" src="/trailers/hd.avi" width="32"></video>

    video_tag("trailer.ogg", "trailer.flv")
    # <video><source src="/videos/trailer.ogg" /><source src="/videos/trailer.flv" /></video>

    video_tag(["trailer.ogg", "trailer.flv"])
    # <video><source src="/videos/trailer.ogg" /><source src="/videos/trailer.flv" /></video>

    video_tag(["trailer.ogg", "trailer.flv"], size: "160x120")
    # <video height="120" width="160"><source src="/videos/trailer.ogg" /><source src="/videos/trailer.flv" /></video>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_tag_helper.rb#L401)
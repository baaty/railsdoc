---
layout: archive_page
---
### 説明
動画ファイルへのパスを取得

### 使い方
    video_path(ファイルへのパス [, オプション])

### オプション

### 例
#### 動画ファイルへのパスを取得
    video_path("hd")
    # /videos/hd

#### 拡張子まで指定
    video_path("hd.avi")
    # /videos/hd.avi

#### 相対パス
    video_path("trailers/hd.avi")
    # /videos/trailers/hd.avi

#### 絶対パス
    video_path("/trailers/hd.avi")
    # /trailers/hd.avi

#### URL
    video_path("http://www.example.com/vid/hd.avi")
    # http://www.example.com/vid/hd.avi

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_url_helper.rb#L400)
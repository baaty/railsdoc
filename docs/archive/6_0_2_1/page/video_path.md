---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_url_helper.rb#L401)
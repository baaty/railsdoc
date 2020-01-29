---
layout: page
---
### 説明
動画ファイルへのパスを取得

### 使い方
    video_path(ファイルへのパス [, オプション])

### オプション

### 例
    video_path("hd")
    # /videos/hd

    video_path("hd.avi")
    # => /videos/hd.avi

    video_path("trailers/hd.avi")
    # => /videos/trailers/hd.avi

    video_path("/trailers/hd.avi")
    # => /trailers/hd.avi

    video_path("http://www.example.com/vid/hd.avi")
    # => http://www.example.com/vid/hd.avi

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/457c876b15640d79f4398c3facb8652210d7c2e0/actionview/lib/action_view/helpers/asset_url_helper.rb#L312)
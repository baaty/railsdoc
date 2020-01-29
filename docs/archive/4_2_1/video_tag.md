---
layout: page
---
### 説明
HTML5で追加されたvideoタグを生成

### 使い方
    video_tag(動画ファイルへのパス, [, オプション])

### オプション

オプション       | 説明
----------- | ------------
:autoplay   | 自動再生を有効
:controls   | コントローラパネルを表示
:loop       | 繰り返し再生
:autobuffer | 自動でバッファリング
:size       | 動画サイズ(幅x高さ)
:width      | 動画の幅
:height     | 動画の高さ
:poster     | サムネイルを表示

### 例
#### 基本形(オプションなし)
    <%= video_tag("test.mp4") %>

#### コントローラパネルを表示
    <%= video_tag("test.mp4", :controls => true) %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L280)
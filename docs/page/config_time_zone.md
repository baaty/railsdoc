---
layout: page
---
### 説明
アプリケーションやアクティブレコードで使用するデフォルトのタイムゾーンの設定

### 使い方
    # config/application.rb
    config.time_zone = 'タイムゾーンの設定'

### タイムゾーン一覧
* [タイムゾーン一覧](http://192.168.11.11:3001/etc#%E3%82%BF%E3%82%A4%E3%83%A0%E3%82%BE%E3%83%BC%E3%83%B3%E4%B8%80%E8%A6%A7)

### 例
#### タイムゾーンを東京に設定
    config.time_zone = 'Tokyo'

### その他
#### 設定できるタイムゾーンの確認
    $ rake time:zones:all

#### 現在のタイムゾーンの確認
    $ rake time:zones:local
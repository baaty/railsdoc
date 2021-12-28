---
layout: page
---
### 説明
アプリケーションやアクティブレコードで使用するデフォルトのタイムゾーンの設定

### 使い方
    config.time_zone = 'タイムゾーンの設定'

### 例
#### タイムゾーンを東京に設定
    config.time_zone = 'Tokyo'

### その他
#### 設定できるタイムゾーンの確認
    $ rake time:zones:all

#### 現在のタイムゾーンの確認
    $ rake time:zones:local
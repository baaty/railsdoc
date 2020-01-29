---
layout: page
---
### 説明
アプリケーションのキャッシュの有無

### 使い方
    config.action_controller.perform_caching = ( true | false )

### デフォルトの設定

環境          | 設定
----------- | -----
development | false
test        | false
production  | true

### 例
    config.action_controller.perform_caching = true
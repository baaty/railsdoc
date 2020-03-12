---
layout: archive_page
---
### 説明
アプリケーションのログレベルを指定

### 使い方
    config.log_level = ( :debug | :info | :warn | :error | :fatal )

### デフォルトの設定

環境          | 設定
----------- | ------------------
development | log_leval = :debug
test        | log_leval = :debug
production  | log_leval = :info

### 例
    config.log_level = :info
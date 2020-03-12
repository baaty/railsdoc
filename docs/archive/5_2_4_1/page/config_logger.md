---
layout: archive_page
---
### 説明
使用するログオブジェクトの種類を指定  
デフォルトでは、ActiveSupport::Loggerのインスタンスを使用

### 使い方
    config.logger = Logger.new(ログのパス, 条件)

### 例
#### 毎日ローテート
    config.logger = Logger.new(config.log_path, 'daily')

#### 10MBごとに10ファイルまで作成
    config.logger = Logger.new(config.log_path, 10, 10.megabytes)

#### ログを無効
    config.logger =nil
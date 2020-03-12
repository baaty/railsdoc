---
layout: archive_page
---
### 説明
電子メールで使用するデフォルトのロガーの設定  
「nil」を設定するとログを出力しない

### 使い方
    config.action_mailer.logger

### 例
    config.action_mailer.logger = ActiveSupport::BufferedLogger.new("mailer.log")
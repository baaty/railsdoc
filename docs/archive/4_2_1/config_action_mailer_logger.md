---
layout: page
---
### 説明
電子メールで使用するデフォルトのロガーの設定をする。「nil」を設定するとログを出力しない

### 使い方
    config.action_mailer.logger = logger

### 例
    config.action_mailer.logger = ActiveSupport::BufferedLogger.new("mailer.log")
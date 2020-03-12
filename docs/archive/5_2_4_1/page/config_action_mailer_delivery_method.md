---
layout: archive_page
---
### 説明
電子メールの配信方法を設定する。デフォルトは、「:smtp」

### 使い方
    config.action_mailer.delivery_method = ( :smtp | :sendmail | :test )

### 例
    config.action_mailer.delivery_method = :sendmail
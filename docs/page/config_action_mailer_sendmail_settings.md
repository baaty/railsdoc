---
layout: page
---

### 説明

sendmailの設定

### 使い方

    config.action_mailer.sendmail_settings = オプション

### オプション

| オプション      | デフォルト値             |
| ---------- | ------------------ |
| :location  | /usr/sbin/sendmail |
| :arguments | -i -t              |

### 例

    config.action_mailer.sendmail_settings = {
      location:  '/usr/sbin/sendmail',
      arguments: '-i -t'
    }

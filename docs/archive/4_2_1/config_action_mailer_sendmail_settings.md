---
layout: page
---
### 説明
sendmailの設定

### 使い方
    config.action_mailer.sendmail_settings = オプション

### オプション
説明実行可能なsendmailのパス。コマンドラインの引数

オプション      | デフォルト
---------- | ------------------
:location  | /usr/sbin/sendmail
:arguments | -i -t

### 例
    config.action_mailer.sendmail_settings = {
      :location       => '/usr/sbin/sendmail',
      :arguments      => '-i -t'
    }
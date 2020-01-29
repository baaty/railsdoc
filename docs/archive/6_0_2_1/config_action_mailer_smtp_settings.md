---
layout: page
---
### 説明
SMTPの設定

### 使い方
    config.action_mailer.smtp_settings

### オプション

オプション           | 説明                                                                                                                                                         | デフォルト
--------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------
:address        | Allows you to use a remote mail server. Just change it from its default "localhost" setting.                                                               | localhost
:port           | On the off chance that your mail server doesn't run on port 25, you can change it.                                                                         | 25
:domain         | If you need to specify a HELO domain, you can do it here.                                                                                                  |
:user_name      | If your mail server requires authentication, set the username in this setting.                                                                             |
:password       | If your mail server requires authentication, set the password in this setting.                                                                             |
:authentication | If your mail server requires authentication, you need to specify the authentication type here. This is a symbol and one of `:plain`, `:login`, `:cram_md5` |

### 例
    config.action_mailer.smtp_settings = {
      address:        'railsdoc.com',
      domain:         'railsdoc.com',
      port:           80,
      user_name:      'example@example.com',
      password:       'yourpassword',
      authentication: :plain
    }
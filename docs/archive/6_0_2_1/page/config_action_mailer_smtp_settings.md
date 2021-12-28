---
layout: page
---
### 説明
SMTPの設定

### 使い方
    config.action_mailer.smtp_settings

### オプション

オプション           | 説明                                              | デフォルト
----------------|---------------------------------------------------|----------
:address        | リモートメールサーバのアドレス                                   | localhost
:port           | ポート番号                                           | 25
:domain         | HELOドメインを指定                                     |
:user_name      | 認証が必要な場合のユーザ名                              |
:password       | 認証が必要な場合のパスワード                              |
:authentication | 認証が必要ば場合の認証タイプ(:plain, :login, :cram_md5) |

### 例
    config.action_mailer.smtp_settings = {
      address:        'railsdoc.com',
      domain:         'railsdoc.com',
      port:           80,
      user_name:      'example@example.com',
      password:       'yourpassword',
      authentication: :plain
    }
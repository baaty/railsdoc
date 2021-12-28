---
layout: page
---
### 説明
電子メールが送信される前に呼び出させるインタープリタを登録

### 使い方
    config.action_mailer.interceptors = インタープリタ

### 例
    config.action_mailer.interceptors = ["MailInterceptor"]
---
layout: page
---
### 説明
条件に一致しなかったらリンクを生成

### 使い方
    mail_to(メールアドレス, [リンクテキスト, オプション])

### オプション

オプション     | 説明
------------ | -----
:subject     | メールの件名
:body        | メールの本文
:cc          | カーボンコピー
:bcc         | ブラインドカーボンコピー
:reply_to    | Reply-Toフィールド

### 例
    mail_to "me@domain.com"
    # <a href="mailto:me@domain.com">me@domain.com</a>

    mail_to "me@domain.com", "My email"
    # <a href="mailto:me@domain.com">My email</a>

    mail_to "me@domain.com", "My email", cc: "ccaddress@domain.com", subject: "This is an example email"
    # <a href="mailto:me@domain.com?cc=ccaddress@domain.com&subject=This%20is%20an%20example%20email">My email</a>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/url_helper.rb#L482)
---
layout: archive_page
---
### 説明
メールアドレス用のタグを生成

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
#### メールアドレス用のタグを生成
    mail_to "me@domain.com"
    # <a href="mailto:me@domain.com">me@domain.com</a>

#### リンクテキストを指定
    mail_to "me@domain.com", "My email"
    # <a href="mailto:me@domain.com">My email</a>

#### オプションを指定
    mail_to "me@domain.com", "My email", cc: "ccaddress@domain.com", subject: "This is an example email"
    # <a href="mailto:me@domain.com?cc=ccaddress@domain.com&subject=This%20is%20an%20example%20email">My email</a>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/url_helper.rb#L482)
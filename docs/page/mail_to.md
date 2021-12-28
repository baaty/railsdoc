---
layout: page
---

### 説明

メールアドレス用のタグを生成

### 使い方

    mail_to(メールアドレス, リンクテキスト=nil, オプション={}, ブロック引数)

### オプション

| オプション | 説明                     |
| ---------- | ------------------------ |
| :subject   | メールの件名             |
| :body      | メールの本文             |
| :cc        | カーボンコピー           |
| :bcc       | ブラインドカーボンコピー |
| :reply_to  | Reply-Toフィールド       |

### 例

#### メールアドレス用のタグを生成

    mail_to "me@domain.com"
    #=> %3Ca+href%3D%22mailto%3Ame%40domain.com%22%3Eme%40domain.com%3C%2Fa%3E

#### リンクテキストを指定

    mail_to "me@domain.com", "My email"
    #=> %3Ca+href%3D%22mailto%3Ame%40domain.com%22%3EMy+email%3C%2Fa%3E

#### オプションを指定

    mail_to "me@domain.com", "My email", cc: "ccaddress@domain.com", subject: "This is an example email"
    #=> %3Ca+href%3D%22mailto%3Ame%40domain.com%3Fcc%3Dccaddress%40domain.com%26subject%3DThis%2520is%2520an%2520example%2520email%22%3EMy+email%3C%2Fa%3E

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/url_helper.rb#L521)

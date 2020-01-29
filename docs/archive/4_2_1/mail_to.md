---
layout: page
---
### 説明
条件に一致しなかったらリンクを生成

### 使い方
    mail_to(メールアドレス, [リンクの文字列, オプション])

### オプション

オプション        | 説明                         | バージョン
------------ | -------------------------- | --------
:subject     | メールの件名                     |
:body        | メールの本文                     |
:cc          | カーボンコピー                    |
:bcc         | ブラインドカーボンコピー               |
:encode      | エンコード方法(:javascript, :hex) | rails3まで
:replace_at  | @のエンコード処理(スパム対策)           | rails3まで
:replace_dot | .のエンコード処理(スパム処理)           | rails3まで

### 例
#### メールアドレスのリンクを表示
    <%= mail_to "railsdoc@example.com" %>
    # <a href="mailto:railsdoc@example.com">railsdoc@example.com</a>

#### 件名とCCを指定してメールアドレスを表示する
    <%= mail_to "railsdoc@example.com", "email", :cc => "railsdoc@example.com", :subject => "test mail" %>
    # <a href="mailto:railsdoc@example.com?cc=railsdoc%40exampe.com&subject=test%20mail">email</a>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/606ce3f907cbccd9159bb558c0b57433b42f3975/actionview/lib/action_view/helpers/url_helper.rb#L456)
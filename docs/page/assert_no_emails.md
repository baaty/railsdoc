---
layout: page
---

### 説明

メールが送信されていないことを確認

### 使い方

    assert_no_emails(ブロック引数)

### 例

#### メールが送信されていないことを確認

    assert_no_emails()

#### ブロック

    assert_no_emails do
        # このブロックからはメールを送信してはいけない
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionmailer/lib/action_mailer/test_helper.rb#L64)

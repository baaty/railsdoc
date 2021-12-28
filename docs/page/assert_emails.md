---
layout: page
---

### 説明

送信されたメールの数が指定された数と一致することを確認

### 使い方

    assert_emails(メール数, ブロック引数)

### 例

#### 送信されたメールの数が指定された数と一致することを確認

    def test_emails
        assert_emails 0
        ContactMailer.welcome.deliver_now
        assert_emails 1
        ContactMailer.welcome.deliver_now
        assert_emails 2
    end

#### ブロック

    def test_emails_again
        assert_emails 1 do
            ContactMailer.welcome.deliver_now
        end
        assert_emails 2 do
            ContactMailer.welcome.deliver_now
            ContactMailer.welcome.deliver_later
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionmailer/lib/action_mailer/test_helper.rb#L34)

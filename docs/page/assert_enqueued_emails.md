---
layout: page
---

### 説明

後で配信するために保留されているメールの数を確認

### 使い方

    assert_enqueued_emails(メール数, ブロック引数)

### 例

#### 後で配信するために保留されているメールの数を確認

    def test_emails
        assert_enqueued_emails 0
        ContactMailer.welcome.deliver_later
        assert_enqueued_emails 1
        ContactMailer.welcome.deliver_later
        assert_enqueued_emails 2
    end

#### ブロック

    def test_emails_again
        assert_enqueued_emails 1 do
            ContactMailer.welcome.deliver_later
        end
        assert_enqueued_emails 2 do
            ContactMailer.welcome.deliver_later
            ContactMailer.welcome.deliver_later
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionmailer/lib/action_mailer/test_helper.rb#L92)

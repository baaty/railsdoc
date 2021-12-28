---
layout: page
---

### 説明

特定のメールがエンキューされたことを確認

### 使い方

    assert_enqueued_email_with(メーラー, メソッド, args: 引数=nil, queue: キュー, ブロック引数)

### 例

#### 特定のメールがエンキューされたことを確認

    def test_email
        ContactMailer.welcome.deliver_later
        assert_enqueued_email_with ContactMailer, :welcome
    end
    def test_email_with_arguments
        ContactMailer.welcome("Hello", "Goodbye").deliver_later
        assert_enqueued_email_with ContactMailer, :welcome, args: ["Hello", "Goodbye"]
    end

#### ブロック

    def test_email_in_block
        assert_enqueued_email_with ContactMailer, :welcome do
            ContactMailer.welcome.deliver_later
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionmailer/lib/action_mailer/test_helper.rb#L126)

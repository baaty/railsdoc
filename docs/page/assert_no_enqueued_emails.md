---
layout: page
---

### 説明

後で配信するために保留されているメールがないことを確認

### 使い方

    assert_no_enqueued_emails(ブロック引数)

### 例

#### 後で配信するために保留されているメールがないことを確認

    assert_no_enqueued_emails()

#### ブロック

    assert_no_enqueued_emails do
        # このブロックからはメールをエンキューしてはいけない
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionmailer/lib/action_mailer/test_helper.rb#L150)

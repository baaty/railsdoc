---
layout: page
---

### 説明

新しいセッションインスタンスを開く

### 使い方

    session = open_session do |sess|
        // 処理内容
    end

### 例

    session = open_session do |sess|
        sess.extend(CustomAssertions)
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/integration.rb#L387)

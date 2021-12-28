---
layout: page
---

### 説明

すべてのエラーメッセージを配列で取得

### 使い方

    モデル.errors.full_messages()

### 例

    person = Person.create(address: '123 First St.')
    person.errors.full_messages
    #=> ["Name is too short (minimum is 5 characters)", "Name can't be blank", "Email can't be blank"]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L383)

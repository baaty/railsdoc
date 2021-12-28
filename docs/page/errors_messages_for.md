---
layout: page
---

### 説明

指定された属性のすべてのエラーメッセージの配列を取得

### 使い方

    モデル.errors.messages_for(属性)

### 例

    person = Person.create()
    person.errors.messages_for(:name)
    #=> ["is too short (minimum is 5 characters)", "can't be blank"]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L412)

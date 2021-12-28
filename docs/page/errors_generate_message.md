---
layout: page
---

### 説明

エラーメッセージをデフォルトのスコープで翻訳

### 使い方

    モデル.errors.generate_message(属性, タイプ=:invalid, オプション={})

### 例

    person = Person.create()
    person.errors.full_messages_for(:name)
    #=> ["Name is too short (minimum is 5 characters)", "Name can't be blank"]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L447)

---
layout: page
---

### 説明

Errorsオブジェクトを取得

### 使い方

    モデル.errors()

### 例

    person = Person.new
    person.valid? #=> false
    person.errors #=> #<ActiveModel::Errors:0x007fe603816640 @messages={name:["can't be blank"]}>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L301)

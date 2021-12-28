---
layout: page
---

### 説明

オブジェクトがモデルを実装するように設計されているか

### 使い方

    to_model()

### 例

    class Person
        include ActiveModel::Conversion
    end
    person = Person.new
    person.to_model == person
    # true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/conversion.rb#L41)

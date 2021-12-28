---
layout: page
---

### 説明

すべての属性名を配列で取得

### 使い方

    to_key()

### 例

    class Person
        include ActiveModel::Conversion
        attr_accessor :id
        def initialize(id)
            @id = id
        end
    end
    person = Person.new(1)
    person.to_key #=> [1]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/conversion.rb#L59)

---
layout: page
---

### 説明

URLでの使用に適したオブジェクトのキーを表す文字列

### 使い方

    to_param()

### 例

    class Person
        include ActiveModel::Conversion
        attr_accessor :id
        def initialize(id)
            @id = id
        end
        def persisted?
            true
        end
    end
    person = Person.new(1)
    person.to_param
    #=> "1"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/conversion.rb#L82)

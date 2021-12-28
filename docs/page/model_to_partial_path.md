---
layout: page
---

### 説明

オブジェクトに関連するパスを示す文字列

### 使い方

    to_partial_path()

### 例

    class Person
        include ActiveModel::Conversion
    end
    person = Person.new
    person.to_partial_path
    #=> "people/person"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/conversion.rb#L95)

---
layout: page
---

### 説明

エラーがないか

### 使い方

    モデル.valid?(コンテキスト=nil)

### 例

#### エラーがないか

    person = Person.new
    person.name = ''
    person.valid? #=> false
    person.name = 'david'
    person.valid? #=> true

#### コンテキスト指定

    person = Person.new
    person.valid?       #=> true
    person.valid?(:new) #=> false

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L334)

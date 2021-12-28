---
layout: page
---

### 説明

エラーが追加されたか

### 使い方

    モデル.invalid?(コンテキスト=nil)

### 例

#### エラーが追加されたか

    person = Person.new
    person.name = ''
    person.invalid? #=> true
    person.name = 'david'
    person.invalid? #=> false

#### コンテキスト指定

    person = Person.new
    person.invalid?       #=> false
    person.invalid?(:new) #=> true

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L373)

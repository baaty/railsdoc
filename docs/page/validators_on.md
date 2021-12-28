---
layout: page
---

### 説明

指定した属性のバリデーションに使用されているすべてのバリデータを一覧表示

### 使い方

    validators_on(属性..)

### 例

    class Person
      include ActiveModel::Validations

      attr_accessor :name , :age

      validates_presence_of :name
      validates_inclusion_of :age, in: 0..99
    end

    Person.validators_on(:name)
    #=> [
    #       <ActiveModel::Validations::PresenceValidator:0x007fe604914e60 @attributes=[:name], @options={}>,
    #    ]


### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L254)

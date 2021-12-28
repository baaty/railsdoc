---
layout: page
---

### 説明

例外的とみなされるバリデーションを定義

### 使い方

    validates!(属性..)

### 例

    class Person
      include ActiveModel::Validations

      attr_accessor :name
      validates! :name, presence: true
    end

    person = Person.new
    person.name = ''
    person.valid?
    #=> ActiveModel::StrictValidationFailed: Name can't be blank

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/validates.rb#L148)

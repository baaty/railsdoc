---
layout: page
---

### 説明

モデルを検証するために使われているすべてのバリデータを取得

### 使い方

    validators()

### 例

    class Person
      include ActiveModel::Validations

      validates_with MyValidator
      validates_with OtherValidator, on: :create
      validates_with StrictValidator, strict: true
    end

    Person.validators
    #=> [
    #      <MyValidator:0x007fbff403e808 @options={}>,
    #      <OtherValidator:0x007fbff403d930 @options={on: :create}>,
    #      <StrictValidator:0x007fbff3204a30 @options={strict:true}>
    #    ]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L192)

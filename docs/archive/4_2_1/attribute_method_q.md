---
layout: page
---
### 説明
メソッドが存在するかチェックする

### 使い方
    モデル.attribute_method?(属性)

### 例
    Person.attribute_method?('name')
    # => true

    Person.attribute_method?(:age=)
    # => true

    Person.attribute_method?(:nothing)
    # => false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/a6157025541c74eea37b626abaeb5af8d69a9d9e/activemodel/lib/active_model/validations.rb#L265)
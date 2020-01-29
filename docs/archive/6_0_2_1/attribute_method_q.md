---
layout: page
---
### 説明
メソッドが存在するかチェック

### 使い方
    モデル.attribute_method?(属性)

### 例
    Person.attribute_method?('name')
    # true

    Person.attribute_method?(:age=)
    # true

    Person.attribute_method?(:nothing)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L142)
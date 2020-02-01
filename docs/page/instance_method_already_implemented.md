---
layout: page
---
### 説明
例外が発生するか？

### 使い方
    モデル.instance_method_already_implemented?(属性)

### 例
#### 例外が発生する
    Person.instance_method_already_implemented?(:save)
    # ActiveRecord::DangerousAttributeError: save is defined by ActiveRecord

#### 例外が発生しない
    Person.instance_method_already_implemented?(:name)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L81)
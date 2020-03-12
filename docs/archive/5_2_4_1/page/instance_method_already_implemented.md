---
layout: archive_page
---
### 説明
例外が発生するかチェック

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L89)
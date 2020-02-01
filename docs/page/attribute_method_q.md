---
layout: page
---
### 説明
指定したレコードが存在するか?

### 使い方
    モデル.attribute_method?(カラム名)

### 例
#### true
    User.attribute_method?(:name)
    # => true

#### false
    User.attribute_method?(:age)
    # => false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L142)
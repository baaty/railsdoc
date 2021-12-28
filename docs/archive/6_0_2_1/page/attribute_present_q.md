---
layout: page
---
### 説明
指定した属性が存在するかチェック

### 使い方
    モデル.attribute_present?(属性名)

### 例
    person.attribute_present?(:title)
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/attribute_methods.rb#L300)
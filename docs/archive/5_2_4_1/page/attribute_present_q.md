---
layout: archive_page
---
### 説明
指定した属性が存在するかチェック

### 使い方
    モデル.attribute_present?(属性名)

### 例
    person.attribute_present?(:title)
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L373)
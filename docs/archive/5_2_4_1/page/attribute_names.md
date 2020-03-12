---
layout: archive_page
---
### 説明
すべての属性名を配列で取得

### 使い方
    モデル.attribute_names()

### 例
#### すべての属性名を配列で取得
    Person.attribute_names
    # ["id", "created_at", "updated_at", "name", "age"]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L314)
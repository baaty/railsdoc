---
layout: page
---
### 説明
モデルに任意のカラムが存在するかチェックする

### 使い方
    モデル.attribute_present?(カラム名)

### 例
    person.attribute_present?(:title)
    # => true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L334)
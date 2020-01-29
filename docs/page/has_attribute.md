---
layout: page
---
### 説明
モデルに任意のカラムが存在するかチェック

### 使い方
    モデル.has_attribute?(属性)

### 例
    person.has_attribute?(:name)
    # true

    person.has_attribute?('age')
    # true

    person.has_attribute?(:nothing)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L259)
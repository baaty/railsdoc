---
layout: page
---
### 説明
モデルに任意のカラムが存在するか

### 使い方
    モデル.has_attribute?(属性)

### 例
#### カラムが存在する場合
    person.has_attribute?(:name)
    # true

#### カラムが存在しない場合
    person.has_attribute?(:nothing)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L259)
---
layout: page
---
### 説明
テーブルの属性を取得する。50文字以降は省略

### 使い方
    モデル.attribute_for_inspect(カラム名)

### 例
    person.attribute_for_inspect(:name)
    # => "\"David Heinemeier Hansson David Heinemeier Hansson D...\""

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L304)
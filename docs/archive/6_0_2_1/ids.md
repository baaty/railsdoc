---
layout: page
---
### 説明
主キーを取得

### 使い方
    モデル.ids

### 例
    Person.ids
    # SELECT people.id FROM people

    Person.joins(:companies).ids
    # SELECT people.id FROM people INNER JOIN companies ON companies.person_id = people.id

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L220)
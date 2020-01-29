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
* [GitHub](https://github.com/rails/rails/blob/b88220732dffe336a0814bb91a4f5acc6e91e508/activerecord/lib/active_record/relation/calculations.rb#L189)
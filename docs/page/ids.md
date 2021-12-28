---
layout: page
---

### 説明

主キーを全て取得

### 使い方

    モデル.ids()

### 例

#### 主キーを全て取得

    Person.ids
    # SELECT people.id FROM people

#### JOIN

    Person.joins(:companies).ids
    # SELECT people.id FROM people INNER JOIN companies ON companies.person_id = people.id

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L242)

---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/calculations.rb#L206)
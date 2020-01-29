---
layout: page
---
### 説明
任意のカラムの配列を取得

### 使い方
    モデル.pluck(カラム名)

### 例
    Person.pluck(:id)
    # SELECT people.id FROM people
    # [1, 2, 3]

    Person.pluck(:id, :name)
    # SELECT people.id, people.name FROM people
    # [[1, 'David'], [2, 'Jeremy'], [3, 'Jose']]

    Person.uniq.pluck(:role)
    # SELECT DISTINCT role FROM people
    # ['admin', 'member', 'guest']

    Person.where(age: 21).limit(5).pluck(:id)
    # SELECT people.id FROM people WHERE people.age = 21 LIMIT 5
    # [2, 3]

    Person.pluck('DATEDIFF(updated_at, created_at)')
    # SELECT DATEDIFF(updated_at, created_at) FROM people
    # ['0', '27761', '173']

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L181)
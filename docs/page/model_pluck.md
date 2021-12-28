---
layout: page
---

### 説明

指定したカラムのレコードの配列を取得

### 使い方

    モデル.pluck(カラム名..)

### 例

#### 指定したカラムのレコードの配列を取得

    Person.pluck(:id)
    # SELECT people.id FROM people

#### 複数指定

    Person.pluck(:id, :name)
    # SELECT people.id, people.name FROM people

#### whereなどと一緒に使用

    Person.where(age: 21).limit(5).pluck(:id)
    # SELECT people.id FROM people WHERE people.age = 21 LIMIT 5

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L192)

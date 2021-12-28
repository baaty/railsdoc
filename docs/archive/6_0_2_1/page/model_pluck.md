---
layout: page
---
### 説明
指定したカラムのレコードの配列を取得

### 使い方
    モデル.pluck(カラム名 [, ...])

### 例
#### 指定したカラムのレコードの配列を取得
    Person.pluck(:id)
    # SELECT people.id FROM people
    # [1, 2, 3]

#### 複数指定
    Person.pluck(:id, :name)
    # SELECT people.id, people.name FROM people
    # [[1, 'David'], [2, 'Jeremy'], [3, 'Jose']]

#### whereなどと一緒に使用
    Person.where(age: 21).limit(5).pluck(:id)
    # SELECT people.id FROM people WHERE people.age = 21 LIMIT 5
    # [2, 3]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L181)
---
layout: page
---
### 説明
条件に一致するレコードを更新

### 使い方
    モデル.update(ID, カラム)

### 例
#### 条件に一致するレコードを更新
    Person.update(15, user_name: "Samuel", group: "expert")

#### ハッシュを使って更新
    people = { 1 => { "first_name" => "David" }, 2 => { "first_name" => "Jeremy" } }
    Person.update(people.keys, people.values)

### 更新メソッドの種類

メソッド              | バリデーションによる検証の有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/78bd18a90992e3da767cfe492f1bc5d63077da8a/activerecord/lib/active_record/relation.rb#L363)
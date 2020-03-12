---
layout: archive_page
---
### 説明
条件に一致するレコードを更新

### 使い方
    モデル.update(ID, 属性)

### 例
#### 条件に一致する属性を更新
    Person.update(15, user_name: "Samuel", group: "expert")

#### ハッシュを使って更新
    people = { 1 => { "first_name" => "David" }, 2 => { "first_name" => "Jeremy" } }
    Person.update(people.keys, people.values)

### 更新メソッドの種類

メソッド              | バリデーションの有無
----------------- | ---------------
update            | ○
update_all        | ×
update_attributes | ○
update_attribute  | ×

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/persistence.rb#L100)
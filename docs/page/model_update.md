---
layout: page
---

### 説明

条件に一致するレコードを更新

### 使い方

    モデル.update(ID=:all, 属性)

    # 失敗したら例外発生
    モデル.update！(ID=:all, 属性)

### 例

#### 条件に一致する属性を更新

    Person.update(15, user_name: "Samuel", group: "expert")

#### ハッシュを使って更新

    people = { 1 => { "first_name" => "David" }, 2 => { "first_name" => "Jeremy" } }
    Person.update(people.keys, people.values)

### 更新メソッドの種類

| メソッド          | バリデーションの有無 |
| ----------------- | -------------------- |
| update            | ○                    |
| update_all        | ×                    |
| update_attributes | ○                    |
| update_attribute  | ×                    |

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L364)

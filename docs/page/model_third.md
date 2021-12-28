---
layout: page
---

### 説明

3番目のレコードを検索

### 使い方

    モデル.third()

    # 失敗したら例外発生
    モデル.third!()

### 例

    Person.third # returns the third object fetched by SELECT * FROM people
    Person.offset(3).third # returns the third object from OFFSET 3 (which is OFFSET 5)
    Person.where(["user_name = :u", { u: user_name }]).third

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L208)

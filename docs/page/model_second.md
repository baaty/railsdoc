---
layout: page
---

### 説明

2番目のレコードを検索

### 使い方

    モデル.second()

    # 失敗したら例外発生
    モデル.second!()

### 例

    Person.second # returns the second object fetched by SELECT * FROM people
    Person.offset(3).second # returns the second object from OFFSET 3 (which is OFFSET 4)
    Person.where(["user_name = :u", { u: user_name }]).second

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L192)

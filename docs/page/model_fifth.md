---
layout: page
---

### 説明

5番目のレコードを検索

### 使い方

    モデル.fifth()

    # 失敗したら例外発生
    モデル.fifth!()

### 例

    Person.fifth # returns the fifth object fetched by SELECT * FROM people
    Person.offset(3).fifth # returns the fifth object from OFFSET 3 (which is OFFSET 7)
    Person.where(["user_name = :u", { u: user_name }]).fifth

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L240)

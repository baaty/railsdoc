---
layout: page
---

### 説明

4番目のレコードを検索

### 使い方

    モデル.fourth()

    # 失敗したら例外発生
    モデル.fourth!()

### 例

    Person.fourth # returns the fourth object fetched by SELECT * FROM people
    Person.offset(3).fourth # returns the fourth object from OFFSET 3 (which is OFFSET 6)
    Person.where(["user_name = :u", { u: user_name }]).fourth

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L224)

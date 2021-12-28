---
layout: page
---

### 説明

最後から3番目のレコードを取得

### 使い方

    モデル.third_to_last()

    # 失敗したら例外発生
    モデル.third_to_last!()

### 例

    Person.third_to_last # returns the third-to-last object fetched by SELECT * FROM people
    Person.offset(3).third_to_last # returns the third-to-last object from OFFSET 3
    Person.where(["user_name = :u", { u: user_name }]).third_to_last

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L272)

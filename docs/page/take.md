---
layout: page
---

### 説明

引数で指定した件数のレコードを取得  
取得するレコードをIDなどで指定することはできない

### 使い方

    モデル.take(件数=nil)

    # 失敗したら例外発生
    モデル.take!(件数=nil)

### 例

#### 1件のレコードを取得

    Person.take
    # SQL: SELECT * FROM people LIMIT 1

#### 2件のレコードを取得

    Person.take(2)
    # SQL: SELECT * FROM people LIMIT 2

#### whereの後に使用

    Person.where(["name LIKE '%?'", name]).take

#### 失敗したら例外発生

    Person.take！

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L287)

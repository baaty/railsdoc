---
layout: page
---

### 説明

引数のプリロードを可能にする

### 使い方

    モデル.preload(引数..)

### 例

    User.preload(:posts)
    # SELECT "posts".* FROM "posts" WHERE "posts"."user_id" IN (1, 2, 3)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L205)

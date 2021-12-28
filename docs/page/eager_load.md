---
layout: page
---

### 説明

左外部結合を使ってすべてのレコードを取得

### 使い方

    モデル.eager_load(属性..)

### 例

    User.eager_load(:posts)
    # SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, ...
    # FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" =
    # "users"."id"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L191)

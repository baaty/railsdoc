---
layout: page
---
### 説明
指定したテーブルのすべてのデータを取得

### 使い方
    モデル.eager_load(属性)

### 例
    User.eager_load(:posts)
    => SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, ...
    FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" =
    "users"."id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L163)
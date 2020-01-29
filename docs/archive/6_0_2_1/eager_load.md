---
layout: page
---
### 説明
指定したテーブルのすべてのデータを取得

### 使い方
    モデル.eager_load(属性)

### 例
    User.eager_load(:posts)
    # SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, ...
    # FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" =
    # "users"."id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L165)
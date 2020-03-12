---
layout: archive_page
---
### 説明
左外部結合を使ってすべてのレコードを取得

### 使い方
    モデル.eager_load(属性)

### 例
#### 左外部結合を使ってすべてのレコードを取得
    User.eager_load(:posts)
    # SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, ...
    # FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" =
    # "users"."id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L133)
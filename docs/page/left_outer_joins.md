---
layout: page
---

### 説明

関連するモデルの左外部結合

### 使い方

    モデル.left_outer_joins(モデル名..)

### 例

    User.left_outer_joins(:posts)
    # SELECT "users".* FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" = "users"."id"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L580)

---
layout: page
---

### 説明

指定したレコードを結果のリレーションから除外

### 使い方

    モデル.excluding(レコード..)

### 例

    Post.excluding(post)
    # SELECT "posts".* FROM "posts" WHERE "posts"."id" != 1

    Post.excluding(post_one, post_two)
    # SELECT "posts".* FROM "posts" WHERE "posts"."id" NOT IN (1, 2)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1226)

---
layout: page
---

### 説明

OR条件式

### 使い方

    モデル.or(条件式)

### 例

#### A or B

    Post.where("id = 1").or(Post.where("author_id = 3"))
    # SELECT `posts`.* FROM `posts` WHERE ((id = 1) OR (author_id = 3))

#### A, B or C

    Post.where(id: 1, name: "名前").or(Post.where(age: nil))
    # SELECT "posts".* FROM "posts" WHERE ("posts"."id" = 1 AND "posts"."name" =  "名前" OR "posts"."age" IS NULL)

#### A or B, C

    Post.where(id: 1).or(Post.where(name: "名前", age: nil))
    # SELECT "posts".* FROM "posts" WHERE ("posts"."id" = 1 OR "posts"."name" =  "名前" AND "posts"."age" IS NULL)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L842)

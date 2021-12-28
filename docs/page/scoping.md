---
layout: page
---

### 説明

すべてのクエリを現在のスコープに収める

### 使い方

    モデル.scoping(all_queries: 全てのクエリ=nil, ブロック引数)

### 例

    Comment.where(post_id: 1).scoping do
        Comment.first
    end
    #=> SELECT "comments".* FROM "comments" WHERE "comments"."post_id" = 1 ORDER BY "comments"."id" ASC LIMIT 1

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L421)

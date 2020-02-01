---
layout: page
---
### 説明
関連するモデルの左外部結合

### 使い方
    モデル.left_outer_joins(モデル名)

### 例
#### 関連するモデルの左外部結合
    User.left_outer_joins(:posts)
    # SELECT "users".* FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" = "users"."id"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L511)
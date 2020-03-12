---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L443)
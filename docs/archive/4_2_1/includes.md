---
layout: page
---
### 説明
関連するテーブルをまとめて取得

### 使い方
    モデル.includes(条件)

### 例
#### 基本的な使い方
    Page.includes(:category)
    # SELECT "pages".* FROM "pages"
    # SELECT "categories".* FROM "categories" WHERE "categories"."id" IN (1)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L144)
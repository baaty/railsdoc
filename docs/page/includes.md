---
layout: page
---
### 説明
関連するテーブルをまとめて取得

### 使い方
    モデル.includes(:モデル [, ...])

### 例
#### 基本的な使い方
    Page.includes(:category)
    # SELECT "pages".* FROM "pages"
    # SELECT "categories".* FROM "categories" WHERE "categories"."id" IN (1)

#### 複数指定
    User.includes(:address, :friends)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L146)
---
layout: page
---
### 説明
データベースから条件を指定し、条件に当てはまるレコードをすべて取得

### 使い方
    モデル.where(条件)

### 例
#### 文字列で指定
    Page.where("category_id = '1'")
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1

#### ハッシュで指定
    Page.where(category_id: 1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1

#### 配列で指定
    Page.where(["category_id = ? and url_id = ?", 1, 1])
    # SELECT "pages".* FROM "pages" WHERE (category_id = 1 and url_id = 1)

#### nilのすべてのデータを取得
    Page.where("title = ?", nil)
    # SELECT "pages".* FROM "pages" WHERE (title = NULL)

#### nilでないすべてのデータを取得
    Page.where("title not ?", nil)
    # SELECT "pages".* FROM "pages" WHERE (title not NULL)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L643)
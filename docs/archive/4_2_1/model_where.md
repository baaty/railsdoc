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
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L568)
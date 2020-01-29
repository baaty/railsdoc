---
layout: page
---
### 説明
カラム名を指定して、検索条件にあうすべてのレコードを取得
rails4からは、whereで代替することができる

### 使い方
    モデル.find_all_by_カラム名(検索する値)

### 例
#### Pagesテーブルのcategory_idが1のすべてのレコードを取得
    Page.find_all_by_category_id(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1
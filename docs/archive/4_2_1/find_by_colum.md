---
layout: page
---
### 説明
カラム名を指定して、最初の1件を取得

### 使い方
    モデル.find_by_カラム名(検索する値)

### 例
#### category_idが1の最初の値を取得
    Page.find_by_category_id(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1 LIMIT 1
---
layout: page
---
### 説明
検索条件を指定して、最初の1件を取得

### 使い方
    モデル.find_by(条件)

### 例
#### category_idが1の最初の値を取得
    Page.find_by category_id: 1
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1 LIMIT 1

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/430a09514a4ad1d0f8481f18a42c4813b6b61e38/activerecord/lib/active_record/relation/finder_methods.rb#L83)
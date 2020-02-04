---
layout: page
---
### 説明
検索条件を指定して、最初の1件を取得

存在しない場合はnil

### 使い方
    モデル.find_by(条件)

### 例
#### category_idが1の最初の値を取得
    Page.find_by category_id: 1
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1 LIMIT 1

#### category_idが1が存在しない場合
    Page.find_by category_id: 1
    # nil

### 補足
* 「find_by!」は存在しない場合に例外を返す

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L80)
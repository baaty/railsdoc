---
layout: page
---
### 説明
取得した値を特定のキーで並び替える

### 使い方
#### 通常
    モデル.order(ソート式)

### 例
#### pagesテーブルをcategory_idで並び替える
    Page.order("category_id")
    # SELECT "pages".* FROM "pages" ORDER BY category_id

    Page.order(:category_id)
    # SELECT "pages".* FROM "pages" ORDER BY category_id

    Page.order("category_id ASC")
    # SELECT "pages".* FROM "pages" ORDER BY category_id ASC

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L317)
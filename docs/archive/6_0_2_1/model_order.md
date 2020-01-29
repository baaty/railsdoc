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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L357)
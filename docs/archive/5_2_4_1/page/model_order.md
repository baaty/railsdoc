---
layout: archive_page
---
### 説明
取得したレコードを特定のキーで並び替える

### 使い方
    モデル.order(:キー名 [ :並び順])
    # または
    モデル.order("キー名 [並び順]")

### 並び順

並び順 | 説明
------|--------------
ASC   | 小さい方から大きい方に並ぶ(昇順)
DESC  | 大きい方から小さい方に並ぶ(降順)

### 例
#### pagesテーブルをcategory_idで並び替える
    Page.order(:category_id)
    # SELECT "pages".* FROM "pages" ORDER BY category_id

#### 昇順で並び替える
    Page.order(:category_id :asc)
    # SELECT "pages".* FROM "pages" ORDER BY category_id ASC

#### 文字列で指定
    Page.order("category_id ASC")
    # SELECT "pages".* FROM "pages" ORDER BY category_id ASC

#### 複数指定
    User.order(:name, email: :desc)
    # SELECT "users".* FROM "users" ORDER BY "users"."name" ASC, "users"."email" DESC

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L290)
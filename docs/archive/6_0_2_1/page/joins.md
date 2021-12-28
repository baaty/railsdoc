---
layout: page
---
### 説明
複数のテーブルを結合して取得

### 使い方
    モデル.joins(条件)

### 例
#### categoryテーブルにpostテーブルを結合して取得
    Category.joins(:posts)
    # SELECT categories.* FROM categories INNER JOIN posts ON posts.category_id = categories.id

#### 2個のテーブルをjoin
    Post.joins(:category, :comments)
    # SELECT posts.* FROM posts
    # INNER JOIN categories ON posts.category_id = categories.id
    # INNER JOIN comments ON comments.post_id = posts.id

#### ネストして結合
    Page.joins(categories: :element)
    #  SELECT "pages".* FROM "pages" INNER JOIN "pages_categories" ON "pages_categories"."page_id" = "pages"."id" INNER JOIN "categories" ON "categories"."id" = "pages_categories"."category_id" INNER JOIN "elements" ON "elements"."id" = "categories"."element_id"

#### SQLで記述
    User.joins("LEFT JOIN bookmarks ON bookmarks.bookmarkable_type = 'Post' AND bookmarks.user_id = users.id")
    # SELECT "users".* FROM "users" LEFT JOIN bookmarks ON bookmarks.bookmarkable_type = 'Post' AND bookmarks.user_id = users.id

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L494)
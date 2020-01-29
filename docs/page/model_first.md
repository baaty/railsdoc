---
layout: page
---
### 説明
テーブルの先頭のレコードを取得

### 使い方
    モデル.first([件数])

### 例
#### pagesテーブルの先頭のレコードを取得
    Page.first
    # SELECT "pages".* FROM "pages" LIMIT 1

#### pagesテーブルの先頭の3つのレコードを取得
    Page.first(3)
    # SELECT "pages".* FROM "pages" LIMIT 3

#### pagesテーブルが空の場合
    Page.first
    # nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L116)
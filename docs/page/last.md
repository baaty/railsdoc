---
layout: page
---
### 説明
テーブルの最後のレコードを取得する

### 使い方
    モデル.last([件数])

### 例

#### pagesテーブルの最後のレコードを取得
    Page.last
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 1

#### pagesテーブルの最後の3つのレコードを取得
    Page.last(3)
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 3

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L145)
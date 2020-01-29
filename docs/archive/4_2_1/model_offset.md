---
layout: page
---
### 説明
特定のレコード位置から取得

### 使い方
    モデル.offset(取得開始位置)

### 例
#### usersテーブルの5件目以降を取得
    Page.offset(5)
    # SELECT "pages".* FROM "pages" LIMIT -1 OFFSET 5

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L636)
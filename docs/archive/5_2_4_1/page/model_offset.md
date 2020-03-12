---
layout: archive_page
---
### 説明
特定のレコード位置から取得

### 使い方
    モデル.offset(取得開始位置)

### 例
#### usersテーブルの5件目以降を取得
    Page.offset(5)
    # SELECT "pages".* FROM "pages" LIMIT -1 OFFSET 5

#### 途中から指定した件数を取得
    User.limit(5).offset(30)
    # SELECT * FROM users LIMIT 5 OFFSET 30

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L678)
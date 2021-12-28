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

#### 途中から指定した件数を取得
    User.limit(5).offset(30)
    # SELECT * FROM users LIMIT 5 OFFSET 30

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L746)
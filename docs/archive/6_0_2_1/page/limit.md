---
layout: page
---
### 説明
取得するレコード数の上限を指定

### 使い方
    モデル.limit(最大取得行数)

### 例
#### usersテーブルから最大5件を取得
    User.limit(5)
    # SELECT * FROM users LIMIT 5

#### 重複する場合あとが優先(最大20件取得)
    User.limit(5).limit(20)
    # SELECT * FROM users LIMIT 20

#### 途中から指定した件数を取得
    User.limit(5).offset(30)
    # SELECT * FROM users LIMIT 5 OFFSET 30

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L730)
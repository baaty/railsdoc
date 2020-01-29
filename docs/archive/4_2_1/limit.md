---
layout: page
---
### 説明
特定のレコード件数を取得

### 使い方
    モデル.limit(最大取得行数)

### 例
#### usersテーブルから最大5件を取得
    User.limit(5)
    # SELECT * FROM users LIMIT 5

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L620)
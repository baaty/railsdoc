---
layout: page
---
### 説明
取得する時のSQLを表示

### 使い方
    モデル.to_sql()

### 例
    User.where(name: 'Oscar').to_sql
    # => SELECT "users".* FROM "users"  WHERE "users"."name" = 'Oscar'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/78bd18a90992e3da767cfe492f1bc5d63077da8a/activerecord/lib/active_record/relation.rb#L536)
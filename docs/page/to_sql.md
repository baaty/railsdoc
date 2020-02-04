---
layout: page
---
### 説明
取得する時のSQLを表示

### 使い方
    モデル.to_sql()

### 例
#### 取得する時のSQLを表示
    User.where(name: 'Oscar').to_sql
    # SELECT "users".* FROM "users"  WHERE "users"."name" = 'Oscar'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L640)
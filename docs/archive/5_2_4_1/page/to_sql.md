---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation.rb#L445)
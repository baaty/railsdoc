---
layout: page
---

### 説明

取得する時のSQLを表示

### 使い方

    モデル.to_sql()

### 例

    User.where(name: 'Oscar').to_sql
    # SELECT "users".* FROM "users"  WHERE "users"."name" = 'Oscar'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L708)

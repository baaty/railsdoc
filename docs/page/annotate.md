---
layout: page
---

### 説明

生成されるクエリにSQLコメントを追加

### 使い方

    モデル.annotate(引数..)

### 例

    User.annotate("selecting user names").select(:name)
    # SELECT "users"."name" FROM "users" /* selecting user names */

    User.annotate("selecting", "user", "names").select(:name)
    # SELECT "users"."name" FROM "users" /* selecting */ /* user */ /* names */

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1184)

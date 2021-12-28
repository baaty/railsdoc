---
layout: page
---

### 説明

特定の値のセットによる順序の指定

### 使い方

    モデル.in_order_of(カラム, 値)

### 例

    User.in_order_of(:id, [1, 5, 3])
    # SELECT "users".* FROM "users" ORDER BY FIELD("users"."id", 1, 5, 3)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L429)

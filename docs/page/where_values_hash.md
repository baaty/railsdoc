---
layout: page
---

### 説明

WHERE条件のハッシュを取得

### 使い方

    モデル.where_values_hash(テーブル名=klass.table_name)

### 例

    User.where(name: 'Oscar').where_values_hash
    #=> {name: "Oscar"}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L675)

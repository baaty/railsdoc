---
layout: page
---

### 説明

SQL文を使って件数を取得

### 使い方

    モデル.count_by_sql(SQL文)

### 例

    Product.count_by_sql "SELECT COUNT(*) FROM sales s, customers c WHERE s.customer_id = c.id"
    # 12

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/querying.rb#L93)

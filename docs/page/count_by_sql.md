---
layout: page
---
### 説明
SQL文を使って件数を取得

### 使い方
    count_by_sql(SQL文)

### 例
    Product.count_by_sql "SELECT COUNT(*) FROM sales s, customers c WHERE s.customer_id = c.id"
    # 12

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/querying.rb#L78)
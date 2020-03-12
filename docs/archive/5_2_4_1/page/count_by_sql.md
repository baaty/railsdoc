---
layout: archive_page
---
### 説明
SQL文を使って件数を取得

### 使い方
    count_by_sql(SQL文)

### 例
    Product.count_by_sql "SELECT COUNT(*) FROM sales s, customers c WHERE s.customer_id = c.id"
    # 12

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/querying.rb#L66)
---
layout: archive_page
---
### 説明
SQL文を直接書いて取得

### 使い方
    モデル.find_by_sql(SQL文)

### 例
#### SQLを直接使って検索
    Page.find_by_sql("SELECT * FROM pages LIMIT 10")
    # SELECT * FROM pages LIMIT 10

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/querying.rb#L40)
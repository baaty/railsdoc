---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/querying.rb#L45)
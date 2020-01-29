---
layout: page
---
### 説明
SQL文を直接書いて、レコードを取得

### 使い方
    モデル.find_by_sql(SQL文)

### 例
#### SQLを直接使って検索
    Page.find_by_sql("SELECT * FROM pages LIMIT 10")
    # SELECT * FROM pages LIMIT 10

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/70d1b5a7f8e25b077168deaf592e0e58c3f2bdd1/activerecord/lib/active_record/querying.rb#L38)
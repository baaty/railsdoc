---
layout: page
---

### 説明

SQL文を直接書いて取得

### 使い方

    モデル.find_by_sql(SQL文, バインド=[], preparable: プレパラート=nil, ブロック引数)

### 例

#### SQL文を直接書いて取得

    Page.find_by_sql("SELECT * FROM pages LIMIT 10")
    # SELECT * FROM pages LIMIT 10

#### 変数でSQL文

    query = "SELECT * FROM pages LIMIT 10"
    Page.find_by_sql(query)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/querying.rb#L49)

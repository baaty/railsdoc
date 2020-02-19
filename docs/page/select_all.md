---
layout: page
---
### 説明
SQL文を直接書いて取得

### 使い方
    select_all(SQL文, [名前, binds, preparable])

### 例
    Client.connection.select_all("SELECT first_name, created_at FROM clients WHERE id = '1'").to_hash
    # [
    #   {"first_name"=>"Rafael", "created_at"=>"2012-11-10 23:23:45.281189"},
    #   {"first_name"=>"Eileen", "created_at"=>"2013-12-09 11:22:35.221282"}
    # ]

### 補足
* find_by_sqlとの違いは取得したオブジェクトのインスタンス化は行わないこと

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L59)
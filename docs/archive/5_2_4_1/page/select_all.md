---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L59)
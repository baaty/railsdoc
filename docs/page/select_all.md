---
layout: page
---

### 説明

SQL文を直接書いて取得

### 使い方

    select_all(SQL文, 名前=nil, バインド=[], プレパラート=nil, async: Async=false)

### 例

    Client.connection.select_all("SELECT first_name, created_at FROM clients WHERE id = '1'").to_hash
    # [
    #   {"first_name"=>"Rafael", "created_at"=>"2012-11-10 23:23:45.281189"},
    #   {"first_name"=>"Eileen", "created_at"=>"2013-12-09 11:22:35.221282"}
    # ]

### 補足

- find_by_sqlとの違いは取得したオブジェクトのインスタンス化は行わないこと

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L62)

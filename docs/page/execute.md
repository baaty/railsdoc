---
layout: page
---

### 説明

マイグレーションファイルでSQLを実行

### 使い方

    execute(SQL文, 名前=nil)

### 例

    execute "SELECT * FROM pages ORDER BY updated_at DESC LIMIT 10"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L116)

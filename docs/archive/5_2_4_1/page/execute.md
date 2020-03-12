---
layout: archive_page
---
### 説明
マイグレーションファイルでSQLを実行

### 使い方
    execute(SQL文)

### 例
#### pagesテーブルの最新の10件を取得
    execute "SELECT * FROM pages ORDER BY updated_at DESC LIMIT 10"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L114)
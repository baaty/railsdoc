---
layout: page
---
### 説明
マイグレーションファイルでSQLを実行

### 使い方
    execute(SQL文)

### 例
#### pagesテーブルの最新の10件を取得
    execute "SELECT * FROM pages ORDER BY updated_at DESC LIMIT 10"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L119)
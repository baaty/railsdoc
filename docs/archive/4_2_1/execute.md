---
layout: page
---
### 説明
マイグレーションファイルでSQLを実行

### 使い方
    execute SQL文

### 例
#### pagesテーブルの最新の10件を取得
    execute "SELECT * FROM pages ORDER BY updated_at DESC LIMIT 10"
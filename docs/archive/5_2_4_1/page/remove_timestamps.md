---
layout: archive_page
---
### 説明
既存のテーブルのcreated_atとupdated_atを削除

### 使い方
    remove_timestamps(テーブル名)

### 例
#### usersテーブルのcreated_atとupdated_atを削除
    remove_timestamps(:users)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1126)
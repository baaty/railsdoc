---
layout: page
---
### 説明
既存のテーブルのcreated_atとupdated_atを削除

### 使い方
    remove_timestamps(テーブル名 [, オプション])

### 例
#### usersテーブルのcreated_atとupdated_atを削除
    remove_timestamps(:users)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1163)
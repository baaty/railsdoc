---
layout: page
---
### 説明
既存のテーブルにcreated_atとupdated_atを追加する

### 使い方
    add_timestamps(テーブル名)

### 例
#### usersテーブルにcreated_atとupdated_atを追加
    add_timestamps(:users)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L876)
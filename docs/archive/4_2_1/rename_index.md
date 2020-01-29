---
layout: page
---
### 説明
指定したテーブルのインデックスを変更

### 使い方
    rename_index(テーブル名, 変更前の名前, 変更後の名前)

### 例
    rename_index :people, 'index_people_on_last_name', 'index_users_on_last_name'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L590)
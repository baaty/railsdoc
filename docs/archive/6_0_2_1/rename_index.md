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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L828)
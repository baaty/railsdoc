---
layout: archive_page
---
### 説明
指定したテーブルのインデックスを変更

### 使い方
    rename_index(テーブル名, 変更前の名前, 変更後の名前)

### 例
#### 指定したテーブルのインデックスを変更
    rename_index :people, 'index_people_on_last_name', 'index_users_on_last_name'

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract_mysql_adapter.rb#L343)
---
layout: archive_page
---
### 説明
指定したテーブルの名前を変更

### 使い方
    rename_table(現在のテーブル名, 新しいテーブル名)

### 例
#### now_tableからnew_tableに変更
    rename_table :now_table, :new_table

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L479)
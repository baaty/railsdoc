---
layout: page
---
### 説明
指定したテーブルの名前を変更

### 使い方
    rename_table(現在のテーブル名, 新しいテーブル名)

### 例
#### now_tableからnew_tableに変更
    rename_table :now_table, :new_table

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/03b304c88588737f55f58952cd6cbe356cd75a90/activerecord/lib/active_record/connection_adapters/abstract_mysql_adapter.rb#L484)
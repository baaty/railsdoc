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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L485)
---
layout: archive_page
---
### 説明
NULL制約の追加または削除

### 使い方
    change_column_null(table_name, column_name, null, default = nil)

### 例
#### 追加
    change_column_null(:users, :nickname, false)

#### 削除
    change_column_null(:users, :nickname, true)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L650)
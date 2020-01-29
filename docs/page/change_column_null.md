---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L661)
---
layout: page
---
### 説明
テーブルに外部キー制約が存在するか

### 使い方
    foreign_key_exists?(from_table [, to_table = nil, オプション])

### 例
#### テーブルに外部キー制約が存在するか
    foreign_key_exists?(:accounts, :branches)

#### カラムを指定
    foreign_key_exists?(:accounts, column: :owner_id)

#### nameを指定
    foreign_key_exists?(:accounts, name: "special_fk_name")

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1048)
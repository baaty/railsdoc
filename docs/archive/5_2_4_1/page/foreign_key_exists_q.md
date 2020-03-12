---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1010)
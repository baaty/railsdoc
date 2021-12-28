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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1085)

---
layout: page
---

### 説明

テーブルに指定した名前のインデックスが存在するか

### 使い方

    index_name_exists?(テーブル名, インデックス名)

### 例

    index_name_exists?(:pages, :title)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L935)

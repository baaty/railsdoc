---
layout: page
---

### 説明

インデックスが存在するか

### 使い方

    index_exists?(カラム名, オプション={})

### 例

    unless t.index_exists?(:branch_id)
        t.index(:branch_id)
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L660)

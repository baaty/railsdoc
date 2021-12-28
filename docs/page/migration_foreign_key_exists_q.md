---
layout: page
---

### 説明

外部キーが存在するか

### 使い方

    foreign_key_exists?(参照元テーブル, 参照先テーブル=nil, オプション引数)

### 例

    t.foreign_key(:authors) unless t.foreign_key_exists?(:authors)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L804)

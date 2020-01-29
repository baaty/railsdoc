---
layout: page
---
### 説明
データベースのカラムを変更する

### 使い方
    change(カラム名, 型 [, オプション])

### 例
    t.change(:name, :string, limit: 80)

    t.change(:description, :text)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0230ad686118b60e89ef8cd2f7b2936099de6deb/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L490)
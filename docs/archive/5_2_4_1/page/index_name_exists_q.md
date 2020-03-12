---
layout: archive_page
---
### 説明
テーブルに指定した名前のインデックスが存在するか

### 使い方
    index_name_exists?(テーブル名, インデックス名)

### 例
#### テーブルに指定した名前のインデックスが存在するか
    index_name_exists?(:pages, :title)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L822)
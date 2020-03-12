---
layout: archive_page
---
### 説明
指定したテーブルの複数のカラムを削除

### 使い方
    remove_columns(テーブル名, カラム名 [, ...])

### 例
#### 指定したテーブルの複数のカラムを削除
    remove_columns(:suppliers, :qualification, :experience)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L588)
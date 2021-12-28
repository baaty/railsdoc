---
layout: page
---
### 説明
指定したテーブルの複数のカラムを削除

### 使い方
    remove_columns(テーブル名, カラム名 [, ...])

### 例
#### 指定したテーブルの複数のカラムを削除
    remove_columns(:suppliers, :qualification, :experience)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L598)
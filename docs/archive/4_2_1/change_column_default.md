---
layout: page
---
### 説明
カラムの初期値を設定する

### 使い方
    change_column_default(テーブル名, カラム名, 初期値)

### 例
    change_column_default(:suppliers, :qualification, 'new')

    change_column_default(:accounts, :authorized, 1)

    change_column_default(:users, :email, nil)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L437)
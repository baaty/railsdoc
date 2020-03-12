---
layout: archive_page
---
### 説明
カラムの初期値を設定

### 使い方
    change_column_default(テーブル名, カラム名, 初期値)

### 例
#### カラムの初期値を設定
    change_column_default(:suppliers, :qualification, 'new')

#### カラムの初期値設定を削除
    change_column_default(:users, :email, nil)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L630)
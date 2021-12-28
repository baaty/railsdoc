---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L641)
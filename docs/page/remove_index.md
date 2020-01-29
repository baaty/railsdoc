---
layout: page
---
### 説明
指定したテーブルのインデックスを削除

### 使い方
    remove_index(テーブル名 [, オプション])

    change_table テーブル名 do |t|
      t.remove_index インデックス名
    end

### オプション

オプション | 説明
------- | -------
:name   | インデックス名
:column | カラム名

### 例
#### usersテーブルのnameカラムのインディックスを削除
    remove_index :users, :name

#### カラム名を指定
    remove_index :accounts, column: :branch_id

#### カラム名を複数指定
    remove_index :accounts, column: [:branch_id, :party_id]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L817)
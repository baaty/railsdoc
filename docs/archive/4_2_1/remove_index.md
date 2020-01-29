---
layout: page
---
### 説明
指定したテーブルのインデックスを削除

### 使い方
    remove_index(テーブル名 [, オプション])

    change_table テーブル名 do |t|
    &nbsp;&nbsp;t.remove_index インデックス名
    end

### オプション

オプション                      | 説明
-------------------------- | -------
:name => インデックス名           | インデックス名
:column => インデックスを構成するカラム名 | カラム名

### 例
#### usersテーブルのnameカラムのインディックスを削除
    remove_index :users, :name

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L576)
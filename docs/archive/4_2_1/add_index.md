---
layout: page
---
### 説明
指定したテーブルにインデックスを追加

### 使い方
    add_index(テーブル名, インデックスを付与するカラム名 [, オプション])

    change_tabe テーブル名 do |t|
        t.index ンデックスを付与するフィールド名 [, オプション]
    end

### オプション

オプション   | 説明
------- | ---------------------
:name   | インデックスの名前
:unique | trueを指定するとユニークなインデックス
:length | インデックスに含まれるカラムの長さ

### 例
#### usersテーブルのnameカラムのインデックスを生成
    add_index :users, :name

#### ユニークなインデックスを生成
    add_index :users, [:name, :employee_id], :unique => true

#### インデックス名をつけて生成
    add_index :users, [:name, :employee_id], :unique => true, :name => 'by_branch_name'

#### インデックスの長さを10に指定して生成
    add_index :users, :name, :name => 'by_name', :length => 10

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L553)
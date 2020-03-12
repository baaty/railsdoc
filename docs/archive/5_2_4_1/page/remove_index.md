---
layout: archive_page
---
### 説明
指定したテーブルのインデックスを削除

### 使い方
    remove_index(テーブル名 [, オプション])

### オプション

オプション      | 説明
-----------|-----------------
:name      | インデックス名
:column    | カラム名
:algorithm | 特定のアルゴリズムのインデックス

### 例
#### usersテーブルのnameカラムのインディックスを削除
    remove_index :users, :name

#### カラム名を指定
    remove_index :accounts, column: :branch_id

#### カラム名を複数指定
    remove_index :accounts, column: [:branch_id, :party_id]

#### インデックス名を指定
    remove_index :accounts, name: :by_branch_party

#### 特定のアルゴリズムのインデックスを指定
    remove_index :accounts, name: :by_branch_party, algorithm: :concurrently

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L786)
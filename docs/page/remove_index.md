---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L817)
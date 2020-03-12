---
layout: archive_page
---
### 説明
指定したテーブルにインデックスを追加

### 使い方
    add_index(テーブル名, インデックスを付与するカラム名 [, オプション])

### オプション

オプション      | 説明                    | データベースの種類
-----------|------------------------|------------------
:name      | インデックスの名前             | 全て
:unique    | trueを指定するとユニークなインデックス | 全て
:length    | インデックスに含まれるカラムの長さ     | 全て
:order     | ソート順                   | MySQL
:where     | 部分インデックス              | PostgreSQL、SQLite
:using     | 特定の方法のインデックス        | PostgreSQL、MySQL
:opclass   | 特定の演算子クラスのインデックス   | PostgreSQL
:type      | 特定のタイプのインデックス         | MySQL
:algorithm | 特定のアルゴリズムのインデックス      | PostgreSQL
:internal  | 長さ制限をするか             | false

### 例
#### usersテーブルのnameカラムのインデックスを作成
    add_index :users, :name

#### ユニークなインデックスを作成
    add_index :users, [:name, :employee_id], unique: true

#### インデックス名をつけて作成
    add_index :users, [:name, :employee_id], unique: true, name: 'by_branch_name'

#### インデックスの長さを10に指定して作成
    add_index :users, :name, name: 'by_name', length: 10

#### 複数のキーで長さを指定
    add_index :accounts, [:name, :surname], name: 'by_name_surname', length: {name: 10, surname: 15}

#### ソート順でインデックスを作成
    add_index :accounts, [:branch_id, :party_id, :surname], order: {branch_id: :desc, party_id: :asc}

#### 部分インデックスの作成
    add_index :accounts, [:branch_id, :party_id], unique: true, where: "active"

#### 特定の方法でインデックスを作成
    add_index :developers, :name, using: 'btree'

#### 特定の演算子クラスでインデックスを作成
    add_index :developers, :name, using: 'gist', opclass: :gist_trgm_ops

#### 特定のタイプのインデックスを作成
    add_index :developers, :name, type: :fulltext

#### 特定のアルゴリズムでインデックスを作成
    add_index :developers, :name, algorithm: :concurrently

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L763)
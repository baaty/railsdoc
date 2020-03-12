---
layout: archive_page
---
### 説明
指定したテーブルにカラムが存在するかチェック

### 使い方
    column_exists?(テーブル名, カラム名 [, 型, オプション])

### オプション

オプション      | 説明                                             | デフォルト値
-----------|------------------------------------------------|-------
:limit     | カラムの桁数を指定                                    |
:default   | デフォルト値を指定                                     |
:null      | NULL値を許可するか                                   | true
:precision | :decimal、:numeric、:datetime、および:time型の精度を指定 |
:scale     | :decimal、:numeric型の小数点以下の桁数              |
:collation | :stringまたは;textの照合順序を指定                    |
:comment   | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能          |

### 例
#### pagesテーブルのtitleカラムが存在するか
    column_exists? :pages, :title

#### suppliersテーブルのnameカラムのstring型が存在するか
    column_exists? :suppliers, :name, :string

#### NULLを許可しない
    column_exists?(:suppliers, :name, :string, null: false)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L132)
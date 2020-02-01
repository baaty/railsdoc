---
layout: page
---
### 説明
指定したテーブルの複数のカラムを削除

### 使い方
    remove_columns(テーブル名, カラム名 [, ...])

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

precisionとscaleについては、データベースによって差があるので注意が必要

### 例
    remove_columns(:suppliers, :qualification, :experience)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L598)
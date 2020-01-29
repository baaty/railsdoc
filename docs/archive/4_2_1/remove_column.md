---
layout: page
---
### 説明
指定したテーブルのカラムを削除

### 使い方
    remove_column(テーブル名, カラム名 [, 型, オプション])

### オプション

オプション      | 説明                  | デフォルト
---------- | ------------------- | -----
:limit     | カラムの桁数を指定           |
:default   | デフォルト値を指定           |
:null      | nill値を許可するか         | true
:precision | :decimal 型の精度を指定    |
:scale     | :decimal 型の小数点以下の桁数 |

### 例
#### usersテーブルのdescriptionカラムを削除
    remove_column(:users, :description)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L414)
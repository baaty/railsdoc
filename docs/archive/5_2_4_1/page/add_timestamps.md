---
layout: archive_page
---
### 説明
既存のテーブルにタイムスタンプ(created_atとupdated_at)を追加

### 使い方
    add_timestamps(テーブル名)

### オプション

オプション      | 説明                                             | デフォルト値
-----------|------------------------------------------------|-------
:limit     | カラムの桁数を指定                                    |
:default   | デフォルト値を指定                                     |
:null      | NULL値を許可するか                                   | false
:precision | :decimal、:numeric、:datetime、および:time型の精度を指定 |
:scale     | :decimal、:numeric型の小数点以下の桁数              |
:comment   | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能          |

### 例
#### usersテーブルにcreated_atとupdated_atを追加
    add_timestamps :users

#### NULLを許可
    add_timestamps :suppliers, null: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1115)
---
layout: page
---
### 説明
指定したテーブルにカラムを追加

### 使い方
    add_column(テーブル名 カラム名, タイプ [, オプション])

#### タイプ
:primary_key、:string、:text、:integer、:bigint、:float、:decimal、:numeric、:datetime、:time、:date、:binary、:boolean
上記以外のデータベース特有のタイプも指定できるが、非推奨

### オプション

オプション      | 説明                                             | デフォルト値
-----------|------------------------------------------------|-------
:limit     | カラムの桁数を指定                                    |
:default   | デフォルト値を指定                                     |
:null      | nill値を許可するか                                   | true
:precision | :decimal、:numeric、:datetime、および:time型の精度を指定 |
:scale     | :decimal、:numeric型の小数点以下の桁数              |
:collation | :stringまたは;textの照合順序を指定                    |
:comment   | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能          |

precisionとscaleについては、データベースによって差があるので注意が必要

### 例
    add_column(:users, :picture, :binary, limit: 2.megabytes)
    # ALTER TABLE "users" ADD "picture" blob(2097152)

    add_column(:articles, :status, :string, limit: 20, default: 'draft', null: false)
    # ALTER TABLE "articles" ADD "status" varchar(20) DEFAULT 'draft' NOT NULL

    add_column(:answers, :bill_gates_money, :decimal, precision: 15, scale: 2)
    # ALTER TABLE "answers" ADD "bill_gates_money" decimal(15,2)

    add_column(:measurements, :sensor_reading, :decimal, precision: 30, scale: 20)
    # ALTER TABLE "measurements" ADD "sensor_reading" decimal(30,20)

    add_column(:measurements, :huge_integer, :decimal, precision: 30)
    # ALTER TABLE "measurements" ADD "huge_integer" decimal(30)

    add_column(:users, :skills, :text, array: true)
    # ALTER TABLE "users" ADD "skills" text[]

    add_column(:shapes, :triangle, 'polygon')
    # ALTER TABLE "shapes" ADD "triangle" polygon

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L588)
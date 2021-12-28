---
layout: page
---

### 説明

指定したテーブルにカラムを追加

### 使い方

    add_column(テーブル名 カラム名, タイプ, オプション引数)

### オプション

| オプション     | 説明                                                           |
| -------------- | -------------------------------------------------------------- |
| :comment       | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能 |
| :collation     | :stringまたは：textの照合順序を指定                            |
| :default       | デフォルト値を指定                                             |
| :limit         | カラムの桁数を指定                                             |
| :null          | NULL値を許可するか                                             |
| :precision     | :decimal、:numeric、:datetime、および:time型の精度を指定       |
| :scale         | :decimal、:numeric型の小数点以下の桁数                         |
| :if_not_exists | カラムがすでに存在している場合は再追加を行わないように指定     |

precisionとscaleについては、データベースによって差があるので注意が必要

### タイプ

| タイプ       | 説明                                                                 |
| ------------ | -------------------------------------------------------------------- |
| :primary_key | プライマリーキー                                                     |
| :string      | 文字列型                                                             |
| :text        | テキスト型                                                           |
| :integer     | 整数型(4バイト)                                                      |
| :bigint      | 整数型(8バイト)                                                      |
| :float       | 浮動小数点数                                                         |
| :decimal     | 固定長整数型                                                         |
| :numeric     | 数値型                                                               |
| :datetime    | 日付と時刻(1000-01-01 00:00:00.000000から9999-12-31 23:59:59.999999) |
| :time        | 時刻 (-838:59:59から838:59:59)                                       |
| :date        | 日付(1000-01-01から9999-12-31)                                       |
| :binary      | バイナリ文字列型                                                     |
| :blob        | Blob                                                                 |
| :boolean     | 真偽値型                                                             |

上記以外のデータベース特有のタイプも指定できるが、非推奨

### 例

#### カラムの追加

    add_column :users, :group_id, :integer

#### カラムの桁数を指定

    add_column :users, :picture, :binary, limit: 2.megabytes
    # ALTER TABLE "users" ADD "picture" blob(2097152)

#### NULLを許可しない

    add_column :articles, :status, :string, limit: 20, default: 'draft', null: false
    # ALTER TABLE "articles" ADD "status" varchar(20) DEFAULT 'draft' NOT NULL

#### 配列を指定

    add_column :users, :skills, :text, array: true
    # ALTER TABLE "users" ADD "skills" text[]

#### 固定長整数型を指定

    add_column :answers, :bill_gates_money, :decimal, precision: 15, scale: 2
    # ALTER TABLE "answers" ADD "bill_gates_money" decimal(15,2)

#### データベース固有のかたを指定

    add_column :shapes, :triangle, 'polygon'
    # ALTER TABLE "shapes" ADD "triangle" polygon

#### カラムが存在する場合はメソッドコールを無視

    add_column(:shapes, :triangle, 'polygon', if_not_exists: true)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L616)

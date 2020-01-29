---
layout: page
---
### 説明
既存のカラムの定義を変更

### 使い方
    change_column(テーブル名,  カラム名, データ型 [, オプション])

### オプション

オプション      | 説明
---------- | -------------------
:limit     | カラムの桁数を指定
:default   | デフォルト値を指定
:null      | nill値を許可するか
:precision | :decimal 型の精度を指定
:scale     | :decimal 型の小数点以下の桁数
:collation | :stringまたは:textの照合順序を指定
:comment   | カラムのコメントを指定。データベース管理ツールなどで閲覧が可能

precisionとscaleについては、データベースによって差があるので注意が必要

### 例
#### usersテーブルのnameカラムをtext型に変更
    change_column(:users, :name, :text)

#### 文字数の最大を80に変更
    change_column(:users, :name, :string, limit: 80)

#### null側を許可しないように変更
    change_column(:users, :name, :string, null: dalse)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L623)
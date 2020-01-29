---
layout: page
---
### 説明
既存のカラムの定義を変更

### 使い方
#### カラムの変更
    change_column(テーブル名,  カラム名, データ型 [, オプション])

#### カラムのデフォルト値の変更
    change_column_default(テーブル名,  カラム名, デフォルト値)

### オプション

オプション      | 説明
---------- | -------------------
:limit     | カラムの桁数を指定
:default   | デフォルト値を指定
:null      | nill値を許可するか
:precision | :decimal 型の精度を指定
:scale     | :decimal 型の小数点以下の桁数

### 例
#### usersテーブルのnameカラムをtext型に変更
    change_column(:users, :name, :text)

#### 文字数の最大を80に変更
    change_column(:users, :name, :string, :limit => 80)

#### null側を許可しないように変更
    change_column(:users, :name, :string, :null => dalse)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L424)
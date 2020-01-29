---
layout: page
---
### 説明
指定したテーブルを削除

### 使い方
    drop_table(:テーブル名 [, オプション])

### オプション

オプション        | 説明                   | デフォルト
------------ | -------------------- | -----
:id          | 主キーを自動生成             | true
:primary_key | 主キーのカラムの名前           | id
:options     | テーブルオプション            |
:temporary   | 一時テーブルとして作成          | false
:force       | テーブルを作成前に、既存のテーブルを削除 | false

### 例
#### productsテーブルを削除
    drop_table :products

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L384)
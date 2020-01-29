---
layout: page
---
### 説明
指定したテーブルにカラムが存在するかチェックする

### 使い方
    column_exists?(テーブル名, カラム名 [, 型, オプション])

### オプション

オプション        | 説明                   | デフォルト
------------ | -------------------- | -----
:id          | 主キーを自動生成             | true
:primary_key | 主キーのカラムの名前           | id
:options     | テーブルオプション            |
:temporary   | 一時テーブルとして作成          | false
:force       | テーブルを作成前に、既存のテーブルを削除 | false

### 例
#### pagesテーブルのtitleカラムにインデックスが存在するか
    column_exists? :pages, :title

### ソースコード
* [GitHub](hhttps://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L76)
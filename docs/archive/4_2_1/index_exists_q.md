---
layout: page
---
### 説明
指定したテーブルにインデックスが存在するかチェック

### 使い方
    index_exists?(テーブル名, カラム名 [, オプション])

### オプション

オプション   | 説明
------- | ---------------------
:name   | インデックスの名前
:unique | trueを指定するとユニークなインデックス
:length | インデックスに含まれるカラムの長さ

### 例
#### pagesテーブルのtitleカラムにインデックスが存在するか
    index_exists? :pages, :title

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L47)
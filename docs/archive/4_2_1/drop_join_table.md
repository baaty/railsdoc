---
layout: page
---
### 説明
join_tableを削除

### 使い方
    drop_join_table(テーブル1, テーブル2 [, オプション])

### オプション

オプション           | 説明
--------------- | --------------------
:table_name     | テーブルの名前
:column_options | カラムのオプション
:options        | オプション
:temporary      | 一時テーブルとして作成
:force          | テーブルを作成前に、既存のテーブルを削除

### 例
    drop_join_table(:assemblies, :parts, options: 'ENGINE=InnoDB DEFAULT CHARSET=utf8')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L282)
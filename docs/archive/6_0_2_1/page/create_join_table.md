---
layout: page
---
### 説明
2つのテーブルを結合して新しいテーブルを作成

### 使い方
    create_join_table(テーブル名1, テーブル名2 [, オプション])

### オプション

オプション           | 説明
--------------- | --------------------
:table_name     | テーブルの名前
:column_options | カラムのオプション
:options        | オプション
:temporary      | 一時テーブルとして作成
:force          | テーブルを作成前に、既存のテーブルを削除

### 例
#### 2つのテーブルを結合して新しいテーブルを作成
    create_join_table(:assemblies, :parts, options: 'ENGINE=InnoDB DEFAULT CHARSET=utf8')
    # CREATE TABLE assemblies_parts (
    #   assembly_id int NOT NULL,
    #   part_id int NOT NULL,
    # ) ENGINE=InnoDB DEFAULT CHARSET=utf8

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L374)
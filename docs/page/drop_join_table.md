---
layout: page
---

### 説明

結合テーブルを削除

### 使い方

    drop_join_table(テーブル1, テーブル2, オプション引数)

### オプション

| オプション      | 説明                                     |
| --------------- | ---------------------------------------- |
| :table_name     | テーブルの名前                           |
| :column_options | カラムのオプション                       |
| :options        | オプション                               |
| :temporary      | 一時テーブルとして作成                   |
| :force          | テーブルを作成前に、既存のテーブルを削除 |

### 例

#### 結合テーブルを削除

    drop_join_table(:assemblies, :parts)

#### オプション指定

    drop_join_table(:assemblies, :parts, options: 'ENGINE=InnoDB DEFAULT CHARSET=utf8')

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L404)

---
layout: page
---

### 説明

2つのテーブルを結合して新しいテーブルを作成

### 使い方

    create_join_table(テーブル名1, テーブル名2, column_options: カラムオプション={}, オプション引数)

### オプション

| オプション      | 説明                                     |
| --------------- | ---------------------------------------- |
| :table_name     | テーブルの名前                           |
| :column_options | カラムのオプション                       |
| :options        | オプション                               |
| :temporary      | 一時テーブルとして作成                   |
| :force          | テーブルを作成前に、既存のテーブルを削除 |

### 例

#### 2つのテーブルを結合して新しいテーブルを作成

    create_join_table(:assemblies, :parts, options: 'ENGINE=InnoDB DEFAULT CHARSET=utf8')

#### ブロック指定

    create_join_table :assemblies, :parts do |t|
      t.index :assemblie_id
      t.index :part_id
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L384)

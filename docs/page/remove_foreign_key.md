---
layout: page
---

### 説明

テーブルから指定された外部キーを削除

### 使い方

    remove_foreign_key(テーブル名, 参照先テーブル名=nil, オプション引数)

### オプション

| 名前      | 説明                             |
| --------- | -------------------------------- |
| :to_table | 参照される主キーを含むテーブル名 |

### 例

#### 外部キーを削除

    remove_foreign_key :accounts, :branches

#### 主キーを含むテーブル名を指定

    remove_foreign_key :accounts, to_table: :owners

#### 名前を指定

    remove_foreign_key :accounts, name: :special_fk_name

#### 外部キーが存在するかどうかをチェックしてから削除

    remove_foreign_key :accounts, :branches, if_exists: true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1126)

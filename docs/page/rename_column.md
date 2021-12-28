---
layout: page
---

### 説明

指定したテーブルのカラム名を変更  
名前を変更しても、そのカラムに関連付けられている既存のデータは破棄されない

### 使い方

    rename_column(テーブル名, 変更するカラム名, 新しいカラム名)

### 例

    rename_column :suppliers, :description, :name

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L725)

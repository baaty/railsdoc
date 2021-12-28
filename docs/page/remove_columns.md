---
layout: page
---

### 説明

指定したテーブルの複数のカラムを削除

### 使い方

    remove_columns(テーブル名, カラム名.., type: 型=nil, オプション引数)

### 例

    remove_columns(:suppliers, :qualification, :experience)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L543)

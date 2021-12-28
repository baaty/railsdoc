---
layout: page
---

### 説明

指定された制約をテーブルから削除

### 使い方

    remove_check_constraint(テーブル名, 制約=nil, オプション引数)

### 例

    remove_check_constraint :products, name: "price_check"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1208)

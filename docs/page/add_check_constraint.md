---
layout: page
---

### 説明

テーブルに新しい制約を追加

### 使い方

    add_check_constraint(テーブル名, 条件, オプション引数)

### オプション

| 名前      | 説明                               | デフォルト値 |
| --------- | ---------------------------------- | ------------ |
| :name     | 制約の名前                         |              |
| :validate | 制約の検証を行うか(PostgreSQLのみ) | true         |

### 例

#### 制約の名前をつけてテーブルに新しい制約を追加

    add_check_constraint :products, "price > 0", name: "price_check"

#### 制約の検証をスキップ

    add_check_constraint :plans, "name IS NOT NULL", name: "plans_name_null", validate: false

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L1185)

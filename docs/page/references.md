---
layout: page
---
### 説明
他のテーブルへの外部キーを表すカラムを生成

### 使い方
    references

### 例
    t.references(:user)
    t.belongs_to(:supplier, foreign_key: true)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L663)
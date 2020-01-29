---
layout: page
---
### 説明
データベースのカラムを変更

### 使い方
    change(カラム名, 型 [, オプション])

### 例
    t.change(:name, :string, limit: 80)

    t.change(:description, :text)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L603)
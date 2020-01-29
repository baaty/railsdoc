---
layout: page
---
### 説明
既存のテーブルのリファレンスを削除

### 使い方
    remove_reference(テーブル名, リファレンス名 [, オプション])

### オプション

オプション        | 説明
------------ | -----------
:polymorphic | ポリモーフィックを付与
:index       | インデックスを付与

### 例
#### オプションなし
    remove_reference(:products, :user, index: true)

#### オプションあり
    remove_reference(:products, :supplier, polymorphic: true)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L677)
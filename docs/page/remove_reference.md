---
layout: page
---
### 説明
既存のテーブルのリファレンスを削除

### 使い方
    remove_reference(テーブル名, リファレンス名 [, オプション])

### オプション

オプション     | 説明
------------ | -----------
:polymorphic | ポリモーフィックを付与
:index       | インデックスを付与
:foreign_key | 外部キーの制約

### 例
#### 既存のテーブルのリファレンスを削除
    remove_reference(:products, :user, index: true)

#### ポリモーフィックを付与
    remove_reference(:products, :supplier, polymorphic: true)

#### 外部キーの制約を指定
    remove_reference(:products, :user, foreign_key: true)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L924)
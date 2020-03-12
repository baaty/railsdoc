---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L893)
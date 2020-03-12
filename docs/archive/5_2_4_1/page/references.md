---
layout: archive_page
---
### 説明
既存のテーブルにリファレンスを追加

### 使い方
    references(カラム名 [, オプション])

### オプション

オプション        | 説明 | デフォルト値
------------ | ----------- | ----
:type        | カラムタイプ         | :bigint
:index       | インデックスを付与    | true
:foreign_key | 外部キーの制約       | false
:polymorphic | ポリモーフィックを付与 | false
:null        | NULLを許可するか     | true

### 例
#### 既存のテーブルにリファレンスを追加
    t.references(:user)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_definitions.rb#L646)
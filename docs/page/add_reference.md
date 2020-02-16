---
layout: page
---
### 説明
既存のテーブルにリファレンスを追加

### 使い方
    add_reference(テーブル名, リファレンス名 [, オプション])

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
    add_reference(:products, :user)

#### 文字列で作成
    add_reference(:products, :user, type: :string)

#### ユニークなインデックス
    add_reference(:products, :supplier, index: { unique: true })

#### 外部キー指定
    add_reference(:products, :supplier, foreign_key: true)

#### NULLを許可しない
    add_reference(:products, :user, null: false)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L904)
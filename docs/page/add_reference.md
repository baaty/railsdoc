---
layout: page
---

### 説明

指定したテーブルにリファレンスを追加

### 使い方

    add_reference(テーブル名, リファレンス名, オプション引数)

### オプション

| オプション   | 説明                   | デフォルト値 |
| ------------ | ---------------------- | ------------ |
| :type        | カラムタイプ           | :bigint      |
| :index       | インデックスを付与     | true         |
| :foreign_key | 外部キーの制約         | false        |
| :polymorphic | ポリモーフィックを付与 | false        |
| :null        | NULLを許可するか       | true         |

### 例

#### リファレンスを追加

    add_reference(:products, :user)

#### 文字列で作成

    add_reference(:products, :user, type: :string)

#### ユニークなインデックス

    add_reference(:products, :supplier, index: { unique: true })

#### NULLを許可しない

    add_reference(:products, :user, null: false)

#### 外部キー指定

    add_reference(:products, :supplier, foreign_key: true)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L988)

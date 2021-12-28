---
layout: page
---
### 説明
指定したテーブルを削除

### 使い方
    drop_table(:テーブル名 [, オプション])

### オプション

オプション      | 説明             | デフォルト値
-----------|----------------|-------
:force     | 依存も削除        | false
:if_exists | 存在する場合のみ削除 | false

### 例
#### productsテーブルを削除
    drop_table :products

#### 依存も削除
    drop_table :care_reasons, force: :cascade

#### 存在する場合のみ削除
    drop_table :article_attributes, if_exists: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L501)
---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L495)
---
layout: archive_page
---
### 説明
指定したテーブルのカラム名を変更  
名前を変更しても、そのカラムに関連付けられている既存のデータは破棄されない

### 使い方
    rename_column(テーブル名, 変更するカラム名, 新しいカラム名)

### 例
#### 指定したテーブルのカラム名を変更
    rename_column :suppliers, :description, :name

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L658)
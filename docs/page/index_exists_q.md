---
layout: page
---
### 説明
指定したテーブルにインデックスが存在するか

### 使い方
    index_exists?(テーブル名, カラム名 [, オプション])

### オプション

オプション   | 説明
------- | ---------------------
:name   | インデックスの名前
:unique | trueを指定するとユニークなインデックス
:length | インデックスに含まれるカラムの長さ

### 例
#### pagesテーブルのtitleカラムにインデックスが存在するか
    index_exists? :pages, :title

#### 複数カラムを指定
    index_exists?(:suppliers, [:company_id, :company_type]

#### ユニークなインデックス
    index_exists?(:suppliers, :company_id, unique: true)

#### インデックス名を指定
    index_exists?(:suppliers, :company_id, name: "idx_company_id")

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L101)
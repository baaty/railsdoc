---
layout: page
---

### 説明

NULL制約の追加または削除

### 使い方

    change_column_null(テーブル名, カラム名, NULL, デフォルト値=nil)

### 例

#### 追加

    change_column_null(:users, :nickname, false)

#### 削除

    change_column_null(:users, :nickname, true)

#### 既存のNULLを空文字に置き換えてNULL制約を追加

    change_column_null(:users, :nickname, false, "")

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L717)

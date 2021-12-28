---
layout: page
---

### 説明

指定したビュー名ががデータベース上に存在するかチェック

### 使い方

    モデル.exists?(条件=:none)

### 例

    view_exists?(:ebooks)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L74)

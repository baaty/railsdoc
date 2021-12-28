---
layout: page
---

### 説明

指定したカラム名のオブジェクトを取得

### 使い方

    モデル.column_for_attribute([カラム名])

### 例

    @page = Page.find(1)
    @page.column_for_attribute(:title)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/model_schema.rb#L460)

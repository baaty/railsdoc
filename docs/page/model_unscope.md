---
layout: page
---

### 説明

条件式を削除

### 使い方

    モデル.unscope(条件式..)

### 例

#### 条件式を削除

    User.order('email DESC').unscope(:order)

#### 複数指定

    User.select(:id).order('email DESC').unscope(:select, :order)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L503)

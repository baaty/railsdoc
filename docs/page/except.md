---
layout: page
---

### 説明

モデルに適応した条件式を除外

### 使い方

    モデル.except(条件式..)

### 例

    Page.order("category DESC").except(:order)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/spawn_methods.rb#L58)

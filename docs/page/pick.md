---
layout: page
---

### 説明

whereやorderなどで取得済みのモデルから先頭のレコードの値を1件取得  
relation.limit(1).pluck().firstの省略形

### 使い方

    pick(カラム名..)

### 例

    User.where(id: 1).pick(:name)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L230)

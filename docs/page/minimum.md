---
layout: page
---

### 説明

カラムの最小値を計算

### 使い方

    モデル.minimum(カラム名)

### 例

    User.minimum('age')
    # SELECT MIN("users"."age") AS min_id FROM "users"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L68)

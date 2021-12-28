---
layout: page
---

### 説明

カラムの最大値を計算

### 使い方

    モデル.maximum(カラム名)

### 例

    User.maximum('age')
    # SELECT MAX("users"."age") AS max_id FROM "users"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L77)

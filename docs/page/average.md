---
layout: page
---

### 説明

カラムの平均値を計算

### 使い方

    モデル.average(カラム名)

### 例

    Page.average(:count)
    # SELECT AVG("pages"."count") AS avg_id FROM "pages"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L59)

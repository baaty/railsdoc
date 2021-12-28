---
layout: page
---

### 説明

カラムの合計値を計算

### 使い方

    モデル.sum(カラム名=nil, ブロック引数)

### 例

    Rating.sum(:score)
    #  SELECT SUM("Ratings"."score") AS sum_id FROM "Ratings"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/calculations.rb#L86)

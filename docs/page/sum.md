---
layout: page
---
### 説明
カラムの合計値を計算

### 使い方
    モデル.sum(カラム名)

### 例
#### Ratingsテーブルのscoreカラムの合計を求める
    Rating.sum(:score)
    #  SELECT SUM("Ratings"."score") AS sum_id FROM "Ratings"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L84)
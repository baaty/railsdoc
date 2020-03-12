---
layout: archive_page
---
### 説明
カラムの合計値を計算

### 使い方
    モデル.sum(カラム名)

### 例
#### Ratingsテーブルのscoreカラムの合計を計算
    Rating.sum(:score)
    #  SELECT SUM("Ratings"."score") AS sum_id FROM "Ratings"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/enumerable.rb#L103)
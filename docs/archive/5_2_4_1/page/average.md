---
layout: archive_page
---
### 説明
カラムの平均値を計算

### 使い方
    モデル.average(カラム名)

### 例
#### 平均を計算
    Page.average(:count)
    # SELECT AVG("pages"."count") AS avg_id FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/calculations.rb#L59)
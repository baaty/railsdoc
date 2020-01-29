---
layout: page
---
### 説明
カラムの平均値を求める

### 使い方
    モデル.average(カラム名 [, オプション])

### 例
#### 平均を求める
    Page.average(:count)
    # SELECT AVG("pages"."count") AS avg_id FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L57)
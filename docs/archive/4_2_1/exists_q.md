---
layout: page
---
### 説明
指定したデータが存在するか

### 使い方
    モデル.exists?(条件)

### 例
#### Pagesテーブルに１件でもデータは存在するか確認
    Page.exists?
    # SELECT 1 FROM "pages" LIMIT 1

#### categoryがrailsであるデータが存在するか確認
    Page.exists?(:category => "rails")
    # SELECT 1 FROM "pages" WHERE "pages"."category" = "rails" LIMIT 1

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/430a09514a4ad1d0f8481f18a42c4813b6b61e38/activerecord/lib/active_record/relation/finder_methods.rb#L289)
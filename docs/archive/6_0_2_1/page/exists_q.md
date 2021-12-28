---
layout: page
---
### 説明
指定したレコードが存在するか

### 使い方
    モデル.exists?([条件])

### 例
#### Pagesテーブルに１件でもデータは存在するか確認
    Page.exists?
    # SELECT 1 FROM "pages" LIMIT 1

#### categoryがrailsであるデータが存在するか確認
    Page.exists?(category: "rails")
    # SELECT 1 FROM "pages" WHERE "pages"."category" = "rails" LIMIT 1

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L300)
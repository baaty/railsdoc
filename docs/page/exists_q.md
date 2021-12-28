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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L326)

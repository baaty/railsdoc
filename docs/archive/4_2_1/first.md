---
layout: page
---
### 説明
テーブルの先頭のレコードを取得

### 使い方
    モデル.first([件数])

### 例
#### pagesテーブルの先頭のレコードを取得
    Page.first
    # SELECT "pages".* FROM "pages" LIMIT 1

#### pagesテーブルの先頭の3つのレコードを取得
    Page.first(3)
    # SELECT "pages".* FROM "pages" LIMIT 3

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L170)
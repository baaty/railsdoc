---
layout: page
---
### 説明
テーブルの最後のレコードを取得する

### 使い方
    モデル.last([件数])

### 例

#### pagesテーブルの最後のレコードを取得
    Page.last
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 1

#### pagesテーブルの最後の3つのレコードを取得
    Page.last(3)
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 3

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L226)
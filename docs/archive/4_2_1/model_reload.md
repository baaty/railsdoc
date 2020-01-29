---
layout: page
---
### 説明
データベースからレコードを再取得する

### 使い方
    モデル.reload

### 例
    @page = Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]
    @page.reload
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L1004)
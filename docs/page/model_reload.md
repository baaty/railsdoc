---
layout: page
---
### 説明
レコードを再取得

### 使い方
    モデル.reload

### 例
#### レコードを再取得
    @page = Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]
    @page.reload
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L1061)
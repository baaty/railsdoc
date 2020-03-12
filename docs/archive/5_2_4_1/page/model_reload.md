---
layout: archive_page
---
### 説明
レコードを再取得

### 使い方
    モデル.reload()

### 例
#### レコードを再取得
    @page = Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]
    @page.reload
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L1064)
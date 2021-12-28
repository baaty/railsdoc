---
layout: page
---

### 説明

レコードを再取得

### 使い方

    モデル.reload(オプション=nil)

### 例

    @page = Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]
    @page.reload
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = ? LIMIT 1  [["id", 1]]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L1067)

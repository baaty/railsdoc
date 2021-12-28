---
layout: page
---

### 説明

モデルの最後のレコードを取得

### 使い方

    モデル.last(件数=nil)

    # 失敗したら例外発生
    モデル.last!(件数=nil)

### 例

#### pagesテーブルの最後のレコードを取得

    Page.last
    # SQL: SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 1

#### 複数を取得

    Page.last(2)
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 2

#### orderで並び替え後のレコードを取得

    Page.order(:title).last
    # SQL: SELECT * FROM pages ORDER BY pages.title DESC LIMIT 1

#### モデルが空の場合

    Page.last
    # nil

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L171)

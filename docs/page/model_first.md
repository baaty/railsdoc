---
layout: page
---

### 説明

モデルの先頭のレコードを取得

### 使い方

    モデル.first(件数=nil)

    # 失敗したら例外発生
    モデル.first!(件数=nil)

### 例

#### モデルの先頭のレコードを取得

    Page.first
    # SQL: SELECT "pages".* FROM "pages" LIMIT 1

#### 複数件数を取得

    Page.first(3)
    # SQL: SELECT "pages".* FROM "pages" LIMIT 3

#### orderで並び替え後のレコードを取得

    Page.order(:title).first
    # SQL: SELECT * FROM pages ORDER BY pages.title ASC LIMIT 1

#### モデルが空の場合

    Page.first
    # nil

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L142)

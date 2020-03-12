---
layout: archive_page
---
### 説明
モデルの先頭のレコードを取得

### 使い方
    モデル.first([件数])

#### 取得するレコードが存在しない場合に例外が発生
    モデル.first!([件数])

### 例
#### モデルの先頭のレコードを取得
    Page.first
    # <Page id: 1, ...>
    # SQL: SELECT "pages".* FROM "pages" LIMIT 1

#### 複数件数を取得
    Page.first(3)
    # [
    #   <Page id: 1, ...>,
    #   <Page id: 2, ...>,
    #   <Page id: 3, ...>
    # ]
    # SQL: SELECT "pages".* FROM "pages" LIMIT 3

#### orderで並び替え後のレコードを取得
    Page.order(:title).first
    # <Page title: a, ...>
    # SQL: SELECT * FROM pages ORDER BY pages.title ASC LIMIT 1

#### モデルが空の場合
    Page.first
    # nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L176)
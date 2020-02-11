---
layout: page
---
### 説明
モデルの最後のレコードを取得

### 使い方
    モデル.last([件数])

#### 取得するレコードが存在しない場合に例外が発生
    モデル.last!([件数])

### 例

#### pagesテーブルの最後のレコードを取得
    Page.last
    # #<Page id: 10, ...>
    # SQL: SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 1

#### 複数を取得
    Page.last(2)
    # [
    #   <Page id: 10, ...>,
    #   <Page id: 9, ...>,
    #   <Page id: 8, ...>
    # ]
    # SELECT "pages".* FROM "pages" ORDER BY "pages"."id" DESC LIMIT 3

#### orderで並び替え後のレコードを取得
    Page.order(:title).last
    # <Page title: z, ...>
    # SQL: SELECT * FROM pages ORDER BY pages.title DESC LIMIT 1

#### モデルが空の場合
    Page.last
    # nil

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/finder_methods.rb#L145)
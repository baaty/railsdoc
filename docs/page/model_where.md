---
layout: page
---
### 説明
条件に当てはまるレコードを全て取得

### 使い方
    モデル.where(条件)

### 例
#### 文字列で指定
    Page.where("category_id = '1'")
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1

#### ハッシュで指定
    Page.where(category_id: 1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1

#### 配列で指定
    Page.where(["category_id = ? and url_id = ?", 1, 1])
    # SELECT "pages".* FROM "pages" WHERE (category_id = 1 and url_id = 1)

#### プレースホルダを使用
    Page.where("category_id = :category_id", {category_id: params[:category_id]})

#### 複数キーを指定
    Page.where(category_id: [1, 2])
    # SELECT * FROM pages WHERE (pages.category_id IN (1,2))

#### NULLのすべてのデータを取得
    Page.where(title: nil)

#### NOT条件
    Page.not.where category_id: 1
    # SELECT * FROM pages WHERE (pages.category_id != 1)

#### AND条件
    Page.where(category_id: 1).where(user_id: 1)

#### OR条件
    Page.where(category_id: 1).or(Page.where(user_id: 1))

#### 範囲指定
    User.where(:id => 1..10)

#### 正規表現
    User.where("name like '%hoge%'")

#### 1年
    User.where(created_at: '2020-1-5'.in_time_zone.all_year)

#### 1月
    User.where(created_at: '2020-1-5'.in_time_zone.all_month)

#### 1日
    User.where(created_at: '2020-1-5'.in_time_zone.all_day)

### 補足
* 文字列で指定する場合は、SQLインジェクションの脆弱性が発生する可能性があるので、外部入力されるキーに関しては配列やプレースホルダを使用してください

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L643)
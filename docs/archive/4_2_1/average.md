---
layout: page
---
### 説明
カラムの平均値を求める

### 使い方
    モデル.average(カラム名 [, オプション])

### オプション

オプション       | 説明
----------- | -------------------------
:conditions | 関数を条件に一致する行に制限
:include    | 関連テーブルのデータを取得
:joins      | テーブル結合
:order      | 結果を並び替える
:select     | 集計に使う行を選択
:distinct   | カラム内の重複した値を除いて、別個の値のみカウント
:group      | グルーピング命令

### 例
#### 平均を求める
    Page.average(:count)
    # SELECT AVG("pages"."count") AS avg_id FROM "pages"

#### カテゴリが1のcountの平均を求める
    Page.average(:count, :conditions => ["category_id = 1"])
    # SELECT AVG("pages"."count") AS avg_id FROM "pages" WHERE (category_id = 1)

#### カテゴリ名がrailsのcountの平均を求める
    Page.average(:count, :joins => :category, :conditions => ["name = 'rails'"])
    # SELECT AVG("pages"."count") AS avg_id FROM "pages" INNER JOIN "categories" ON "categories"."id" = "pages"."category_id" WHERE (name = 'rails')

#### カテゴリごとにグルーピングして、平均を求める
    Page.average(:count, :group => :category_id)
    # SELECT AVG("pages"."count") AS average_position, category_id AS category_id FROM "pages" GROUP BY category_id

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/b88220732dffe336a0814bb91a4f5acc6e91e508/activerecord/lib/active_record/relation/calculations.rb#L49)
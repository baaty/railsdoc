---
layout: page
---
### 説明
データベースからデータを検索する

### 注意
rails3からrails4で大きく変更があったメソッドの一つ
find(:all)やfind(:all, :conditions ...)などの書き方が廃止になりました。whereなどを使うようにしてください
activerecord-deprecated_findersというgemを使うことで使えるようになりますが、推奨されていないようです

### 使い方
#### rails4
##### 1つのレコードを取得
    モデル.find(引数)

##### 配列を使ってレコードを取得
    モデル.find(配列)

#### rails3
##### 1つのレコードを取得
    モデル.find(:id [, オプション])

##### 配列を使ってレコードを取得
    モデル.find(配列 [, オプション])

##### テーブルの先頭行を取得
    モデル.find(:first, [オプション])

##### テーブルの最終行を取得
    モデル.find(:last,[オプション])

##### テーブルの全データを取得
    モデル.find(:all, [オプション])

### オプション

オプション      | 説明                           | バージョン
---------- | ---------------------------- | --------
:condition | 検索条件を指定                      | rails3まで
:offset    | オフセット値                       | rails3まで
:limit     | 取得件数                         | rails3まで
:order     | ソート                          | rails3まで
:select    | 取得したデータのカラム                  | rails3まで
:group     | グルーピング命令                     | rails3まで
:joins     | テーブル結合                       | rails3まで
:include   | 関連テーブルのデータを取得                | rails3まで
:readonly  | trueが設定されていると、保存できない         | rails3まで
:from      | selectに挿入されるテーブル名をオーバーライトできる | rails3まで
:lock      | データベースにロック                   | rails3まで

### 保存できない場合

メソッド名        | 保存できない場合
------------ | --------
find(:id)    | 例外
find(配列)     | 例外
find(:first) | nil
find(:last)  | nil
find(:all)   | 空の配列

### 例
#### rails4
##### IDで検索
    Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = 1 LIMIT 1

##### 複数の項目をIDで検索
    Page.find([1, 2])
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" IN (1, 2)

#### rails3
##### IDで検索
    Page.find(1)
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" = 1 LIMIT 1

##### 複数の項目をIDで検索
    Page.find([1, 2])
    # SELECT "pages".* FROM "pages" WHERE "pages"."id" IN (1, 2)

##### すべての項目を取得
    Page.find(:all)
    # SELECT "pages".* FROM "page"

##### はじめにヒットした項目を取得
    Page.find(:first)
    # SELECT "pages".* FROM "pages" LIMIT 1

##### 最後にヒットした項目を取得
    Page.find(:last)
    # SELECT "pages".* FROM "pages" ORDER BY pages.id DESC LIMIT 1

##### 特定のカラムのみロード
    Page.find(:first, :select => "name, content")
    # SELECT name, content FROM "pages" LIMIT 1

##### category_idが1のすべてのレコードを取得
    Page.find(:all, :conditions => { :category_id => 1 })
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1

##### category_idが1でurl_idが1のすべてのレコードを取得
    Page.find(:all, :conditions => ["category_id = ? and url_id = ?", 1, 1])
    # SELECT "pages".* FROM "pages" WHERE (category_id = 1 and url_id = 1)

##### titleがnilでないすべてのレコードを取得
    Page.find(:all, :conditions => ["category_id NOT ?", nil])
    # SELECT "pages".* FROM "pages" WHERE (title NOT NULL)

##### category_idが1のはじめのレコードを取得
    Page.find(:first, :conditions => {:category_id => 1})
    # SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1 LIMIT 1

##### 検索結果の並び順を変更
    Page.find(:all, :order => "created_at DESC")
    # SELECT "pages".* FROM "pages" ORDER BY created_at DESC

##### 検索結果の取得件数を指定
    Page.find(:all, :limit => 3)
    # SELECT "pages".* FROM "pages" LIMIT 3

##### 読み飛ばし件数を指定
    Page.find(:all, :offset => 20, :limit => 10)
    # SELECT "pages".* FROM "pages" LIMIT 10 OFFSET 20

##### SQLのJOIN句の文字列を指定
    Page.find(:first, :joins => :category)
    # SELECT "pages".* FROM "pages" INNER JOIN "categories" ON "categories"."id" = "pages"."category_id" LIMIT 1

##### SQLのGROUP BY句の文字列を指定
    Page.find(:all, :group => "category_id")
    # SELECT "pages".* FROM "pages" GROUP BY category_id

##### テーブルを結合して、情報をロード
    Page.find(:all, :include => "category")
    # SELECT "pages".* FROM "pages"
    # SELECT "categories".* FROM "categories" WHERE ("categories"."id" IN (1,2,3)

### その他
#### SQLインジェクション対策
外部から渡される値は、エスケープしてデータベースに渡す

#### 使い方
    ["カラム名 = ?", 検索する値]

#### 例
##### 外部から入力された値を使う場合
    params[:user]user = User.find(:all, :conditions => ["name = ?", name])

##### 検索条件としてハッシュのキーとバリューを使う場合
    User.find(:all, :conditions => params[:user]]

#### ワイルドカードでデータベースを検索
##### 使い方
    like

##### 例
    User.find(:all, :conditions => ["name like ?", params[:name]+"%"])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/430a09514a4ad1d0f8481f18a42c4813b6b61e38/activerecord/lib/active_record/relation/finder_methods.rb#L67)
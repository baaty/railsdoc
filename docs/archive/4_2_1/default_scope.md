---
layout: page
---
### 説明
デフォルトのスコープを定義

### 使い方
    default_scope(条件式 [, オプション])

### オプション

オプション      | 説明
---------- | ----------------------------
:condition | 検索条件を指定
:offset    | オフセット値
:limit     | 取得件数
:order     | ソート
:select    | 取得したデータのカラム
:group     | グルーピング命令
:joins     | テーブル結合
:include   | 関連テーブルのデータを取得
:readonly  | trueが設定されていると、保存できない
:from      | selectに挿入されるテーブル名をオーバーライトできる
:lock      | データベースにロック

### 例
    class Article < ActiveRecord::Base
      default_scope { where(published: true) }
    end

    Article.all # => SELECT * FROM articles WHERE published = true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/c81e4e6a2657f3f67b99a2f88e2909c36c9f3863/activerecord/lib/active_record/scoping/default.rb#L83)
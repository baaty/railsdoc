---
layout: page
---
### 説明
カラムの合計値を求める

### 使い方
    モデル.sum(カラム名[, オプション])

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
#### Ratingsテーブルのscoreカラムの合計を求める
    Rating.sum(:score)
    #  SELECT SUM("Ratings"."score") AS sum_id FROM "Ratings"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/a476020567a47f5fbec3629707d5bf31b400a284/activesupport/lib/active_support/core_ext/enumerable.rb#L20)
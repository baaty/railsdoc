---
layout: archive_page
---
### 説明
カラムの最大値を計算

### 使い方
    モデル.maximum(カラム名 [, オプション])

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
#### usersテーブルのageカラムの最大値を計算
    User.maximum('age')
    # SELECT MAX("users"."age") AS max_id FROM "users"

#### 条件を指定
    Account.maximum(:limit, :conditions => "limit > 50")

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/calculations.rb#L77)
---
layout: page
---
### 説明
カラムの最小値を求める

### 使い方
    モデル.minimum(カラム名 [, オプション])

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
#### usersテーブルのageカラムの最小値を求める
    User.minimum('age')
    # SELECT MIN("users"."age") AS min_id FROM "users"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/b88220732dffe336a0814bb91a4f5acc6e91e508/activerecord/lib/active_record/relation/calculations.rb#L60)
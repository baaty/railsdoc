---
layout: page
---
### 説明
カラムを処理

### 使い方
    モデル.calculate(条件, カラム名 [, オプション])

### オプション

オプション    | 説明
----------- | -------------------------
:conditions | 関数を条件に一致する行に制限
:include    | 別のテーブルとのインクルードを指定
:joins      | 別のテーブルとの結合を指定
:order      | 結果を並び替える
:group      | グルーピング命令
:select     | 集計に使う行を選択
:distinct   | カラム内の重複した値を除いて、別個の値のみカウント

### 例
#### pagesテーブルのカラム数
    Page.calculate(:count, :all)
    # SELECT COUNT(*) FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/b88220732dffe336a0814bb91a4f5acc6e91e508/activerecord/lib/active_record/relation/calculations.rb#L117)
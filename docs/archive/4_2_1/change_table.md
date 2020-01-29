---
layout: page
---
### 説明
テーブル定義を変更する

### 使い方
    change_table(テーブル名 [, オプション]) do |t|
      t.メソッド名(データ型) カラム名
    end

### オプション

オプション | 説明                        | デフォルト
----- | ------------------------- | -----
:bulk | 変更内容を1つのALTER TABLEにまとめるか | false

### 使用できるメソッド

メソッド名             | 説明
----------------- | -------------
index             | インデックス
change            | カラムを変更
change_default    | カラムのデフォルト値を変更
rename            | カラムの名前を変更
remove            | カラムを削除
remove_references | リファレンスの削除
remove_index      | インデックスの削除
remove_timestamps | タイムスタンプの削除

### データ型

メソッド名     | 説明
--------- | --------
string    | 文字列
text      | 長い文字列
integer   | 整数
float     | 浮動小数
decimal   | 精度の高い小数
datetime  | 日時
timestamp | より細かい日時
time      | 時間
date      | 日付
binary    | バイナリデータ
boolean   | Boolean型

### 例
#### pagesテーブルにtext型のmemoを追加、titleにインデックスを設定
    change_table :pages do |t|
      t.text :memo
      t.index :title
    end

#### カラムの追加
    change_table(:suppliers) do |t|
      t.column :name, :string, limit: 60
    end

#### 2つのカラムの追加
    change_table(:suppliers) do |t|
      t.integer :width, :height, null: false, default: 0
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/7785417984f61a9d5e00416c13b89dce2ee02daf/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L357)
---
layout: archive_page
---
### 説明
テーブル定義を変更

### 使い方
    change_table(テーブル名 [, オプション]) do |t|
      t.メソッド名(データ型) カラム名
    end

### オプション

オプション | 説明                          | デフォルト値
------|-----------------------------|-------
:bulk | 変更内容を1つのALTER TABLEにまとめるか | false

### 使用できるメソッド

メソッド名            | 説明
------------------|--------------
index             | インデックス
change            | カラムを変更
change_default    | カラムのデフォルト値を変更
column            | カラムの追加
rename            | カラムの名前を変更
timestamps        | タイムスタンプを追加
belongs_to        | 関係を追加
remove            | カラムを削除
remove_references | リファレンスの削除
remove_index      | インデックスの削除
remove_timestamps | タイムスタンプの削除
references        | 外部キーを追加

### データ型

型        | 説明
----------|---------
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

#### タイムスタンプを追加
    change_table(:suppliers) do |t|
      t.timestamps
    end

#### 外部キーを追加
    change_table(:suppliers) do |t|
      t.references :company
    end

#### 複数カラムの削除
    change_table(:suppliers) do |t|
      t.remove :company_id
      t.remove :width, :height
    end

#### インデックスを削除
    change_table(:suppliers) do |t|
      t.remove_index :company_id
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/connection_adapters/abstract/schema_statements.rb#L465)
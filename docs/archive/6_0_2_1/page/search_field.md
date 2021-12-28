---
layout: page
---
### 説明
検索ボックスを生成

### 使い方
    search_field(オブジェクト名, メソッド名 [, オプション])

#### f.object
    f.search_field(メソッド名 [, オプション])

### オプション

オプション      | 説明
-----------|-------------------
:autosave  | オートセーブ
:results   | 表示される最大数
:onsearch  | インクリメンタルサーチ
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:disabled  | 無効化
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### search_field
##### 検索ボックスを生成
    search_field(:user, :name)
    # <input id="user_name" name="user[name]" type="search" />

##### 表示される最大数を3
    search_field(:user, :name, results: 3)
    # <input id="user_name" name="user[name]" results="3" type="search" />

##### オートセーブ
    search_field(:user, :name, autosave: true)
    # <input autosave="com.example.www" id="user_name" name="user[name]" results="10" type="search" />

##### インクリメンタルサーチ
    search_field(:user, :name, onsearch: true)
    # <input id="user_name" incremental="true" name="user[name]" onsearch="true" type="search" />

#### f.search_field
##### 検索ボックスを生成
    f.search_field :name

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1353)
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1748)
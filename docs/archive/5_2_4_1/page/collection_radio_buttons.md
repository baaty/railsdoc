---
layout: archive_page
---
### 説明
モデルからラジオボタンを自動生成

### 使い方
    collection_radio_buttons(オブジェクト名, コレクション名, メソッド名, value値 [, オプション])

#### f.object
    f.collection_radio_buttons(メソッド名, コレクション名, value値 [, オプション])

### オプション

オプション   | 説明
---------- | ------------------
:checked   | チェックの有無
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
#### collection_radio_buttons
##### モデルからラジオボタンを自動生成
    collection_radio_buttons(:post, :author_id, Author.all, :id, :name_with_initial)

##### ブロックで指定
    collection_radio_buttons(:post, :author_id, Author.all, :id, :name_with_initial) do |b|
      b.label { b.radio_button }
    end

#### f.collection_radio_buttons
##### モデルからラジオボタンを自動生成
    form_for @post do |f|
      f.collection_radio_buttons :author_id, Author.all, :id, :name_with_initial
      f.submit
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L672)
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L882)
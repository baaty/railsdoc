---
layout: page
---
### 説明
URL入力ボックスを生成

### 使い方
    url_field(オブジェクト名, メソッド名 [, オプション])

#### f.object
    f.url_field(メソッド名 [, オプション])

### オプション

オプション   | 説明
---------- | ------------------
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
#### url_field
##### URL入力ボックスを生成
    url_field("user", "homepage")
    # <input id="user_homepage" name="user[homepage]" type="url" />

#### f.url_field
##### URL入力ボックスを生成
    f.url_field("user", "homepage")
    # <input id="user_homepage" name="user[homepage]" type="url" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1497)
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1865)
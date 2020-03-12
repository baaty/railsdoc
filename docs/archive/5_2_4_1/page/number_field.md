---
layout: archive_page
---
### 説明
数値入力ボックスを生成

### 使い方
    number_field(オブジェクト名, メソッド名 [, オプション])

### オプション

オプション      | 説明
---------- | ------------------
:min       | 最少値
:max       | 最大値
:in        | 最少値から最大値
:step      | 許容値の粒度
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
#### 数値入力ボックスを生成
    number_field :product, :price

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_helper.rb#L1508)
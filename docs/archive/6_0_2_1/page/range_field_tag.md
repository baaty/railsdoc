---
layout: page
---
### 説明
モデルと関連のない範囲選択バーを生成

### 使い方
    range_field_tag(要素名 [, 値, オプション])

### オプション

オプション   | 説明
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
#### 範囲選択バーを生成
range_field_tag :volume

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L815)
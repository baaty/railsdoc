---
layout: page
---
### 説明
月の入力欄を生成

### 使い方
    month_field_tag(要素名 [, 値, オプション or HTMLオプション])

### オプション

オプション | 説明
------|-------
:min  | 最少値
:max  | 最大値
:step | 許容値の粒度

### HTMLオプション

オプション        | 説明
-------------|--------------------
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列
:accept      | フォームで受付可能なMIMEタイプ
:readonly    | フォームの内容変更禁止
:tabindex    | Tabキーによる入力欄の移動順
:accesskey   | フォームに移動するショートカットキー
:id          | 要素固有の識別子
:class       | 要素を分類するクラス名
:title       | 要素の補足情報
:style       | 要素の補足情報
:dir         | 表記方向
:lang        | 基本言語

### 例
#### 月のテキストフィールドを生成
    month_field_tag :published_month

#### 最小値を設定
    month_field_tag(:published_month, :min => DateTime.new(2020, 1, 1)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L704)
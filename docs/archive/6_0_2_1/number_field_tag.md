---
layout: page
---
### 使い方
    number_field_tag(要素名 [, 値, オプション])

#### オプション

オプション      | 説明
---------- | ------------------
:min       | 最少許容値
:max       | 最大許容値
:in        | 最少許容値から最大許容値
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

#### 例
    number_field_tag 'quantity'
    # <input id="quantity" name="quantity" type="number" />

    number_field_tag 'quantity', '1'
    # <input id="quantity" name="quantity" type="number" value="1" />

    number_field_tag 'quantity', nil, class: 'special_input'
    # <input class="special_input" id="quantity" name="quantity" type="number" />

    number_field_tag 'quantity', nil, min: 1
    # <input id="quantity" name="quantity" min="1" type="number" />

    number_field_tag 'quantity', nil, max: 9
    # <input id="quantity" name="quantity" max="9" type="number" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L802)
---
layout: page
---
### 使い方
    number_field_tag(要素名 [, 値, オプション])

#### 使用できるフォームタグ
* form_for
* form_tag

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
:disabled  | フォームの項目の利用禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
    number_field_tag 'quantity', nil, in: 1...10
    # => <input id="quantity" name="quantity" min="1" max="9" type="number" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L786)

### number_fieldとnumber_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
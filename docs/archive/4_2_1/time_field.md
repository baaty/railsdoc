---
layout: page
---
### time_field
#### 説明
時間の入力欄を生成

#### 使い方
    time_field(要素名 [, 値, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
:min       | 最少許容値
:max       | 最大許容値
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


#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1067)

### f.time_field
#### 説明
時間の入力欄を生成

#### 使い方
    f.time_field(要素名 [, 値, オプション])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション      | 説明
---------- | ------------------
:min       | 最少許容値
:max       | 最大許容値
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

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1067)

### time_fieldとtime_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
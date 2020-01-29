---
layout: page
---
### color_field
#### 説明
色の入力欄を生成

#### 使い方
    color_field(オブジェクト名, メソッド名 [, オプション or HTMLオプション])

#### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

#### HTMLオプション

オプション      | 説明
-----------|-------------------
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
##### 色の入力欄を生成
    color_field "car", "color"
    # <input id="car_color" name="car[color]" type="color" value="#000000" />

##### カラーコード指定
    color_field "car", "color", "#DEF726"
    # <input id="car_color" name="color" type="color" value="#DEF726" />

##### HTMLオプション指定
    color_field "car", "color", nil, class: 'special_input'
    # <input class="special_input" id="car_color" name="color" type="color" />

##### フォームの項目の利用禁止
    color_fiel "car", "color", "DEF726", class: "special_input", disabled: true
    # <input disabled="disabled" class="special_input" id="car_color" name="color" type="color" value="#DEF726" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1330)

### f.color_field
#### 説明
色の入力欄を生成

#### 使い方
    f.color_field(メソッド名 [, オプション or HTMLオプション])

#### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

#### HTMLオプション

オプション      | 説明
-----------|-------------------
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
##### 色の入力欄を生成
    f.color_field("car", "color")
    # <input id="car_color" name="car[color]" type="color" value="#000000" />

##### カラーコード指定
    f.color_field "car", "color", "#DEF726"
    # <input id="car_color" name="color" type="color" value="#DEF726" />

##### HTMLオプション指定
    f.color_field "car", "color", nil, class: 'special_input'
    # <input class="special_input" id="car_color" name="color" type="color" />

##### フォームの項目の利用禁止
    f.color_fiel "car", "color", "DEF726", class: "special_input", disabled: true
    # <input disabled="disabled" class="special_input" id="car_color" name="color" type="color" value="#DEF726" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1735)
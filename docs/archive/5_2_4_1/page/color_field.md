---
layout: archive_page
---
### 説明
色の入力欄を生成

### 使い方
    color_field(オブジェクト名, メソッド名 [, オプション or HTML属性 or イベント属性])

### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

### HTML属性

HTML属性      | 説明
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

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### color_field
##### 色の入力欄を生成
    color_field "car", "color"
    # <input id="car_color" name="car[color]" type="color" value="#000000" />

##### カラーコード指定
    color_field "car", "color", "#DEF726"
    # <input id="car_color" name="color" type="color" value="#DEF726" />

##### プション指定
    color_field "car", "color", nil, class: 'special_input'
    # <input class="special_input" id="car_color" name="color" type="color" />

##### フォームの項目の利用禁止
    color_fiel "car", "color", "DEF726", class: "special_input", disabled: true
    # <input disabled="disabled" class="special_input" id="car_color" name="color" type="color" value="#DEF726" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_helper.rb#L1324)
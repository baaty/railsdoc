---
layout: page
---
### 説明
テキストボックスを生成

### 使い方
    text_field_tag(要素名 [, value値, オプション or HTML属性 or イベント属性])

### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | 幅
:maxlength   | 入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

### HTML属性

HTML属性   | 説明
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
#### 基本的な使い方
    text_field_tag 'name'
    # <input id="name" name="name" type="text" />

#### 値を指定
    text_field_tag 'query', 'Enter your search query here'
    # <input id="query" name="query" type="text" value="Enter your search query here" />

#### フォーカスが当たるまでデフォルト表示される文字列を指定
    text_field_tag 'search', nil, placeholder: 'Enter search term...'
    # <input id="search" name="search" placeholder="Enter search term..." type="text" />

#### HTML属性を指定
    text_field_tag 'request', nil, class: 'special_input'
    # <input class="special_input" id="request" name="request" type="text" />

#### サイズを指定
    text_field_tag 'address', '', size: 75
    # <input id="address" name="address" size="75" type="text" value="" />

#### 最大文字数を指定
    text_field_tag 'zip', nil, maxlength: 5
    # <input id="zip" maxlength="5" name="zip" type="text" />

#### 無効化
    text_field_tag 'payment_amount', '$0.00', disabled: true
    # <input disabled="disabled" id="payment_amount" name="payment_amount" type="text" value="$0.00" />

#### オプションとHTML属性を指定
    text_field_tag 'ip', '0.0.0.0', maxlength: 15, size: 20, class: "ip-input"
    # <input class="ip-input" id="ip" maxlength="15" name="ip" size="20" type="text" value="0.0.0.0" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L197)
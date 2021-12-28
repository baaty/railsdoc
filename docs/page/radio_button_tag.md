---
layout: page
---

### 説明

モデルと関連のないラジオボタンを生成

### 使い方

    radio_button_tag(要素名, value値, checked=false, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション | 説明   |
| ---------- | ------ |
| :disabled  | 無効化 |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :checked   | チェックの有無                       |
| :size      | フォームの幅                         |
| :maxlength | 入力フィールドに入力可能な最大文字数 |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### イベント属性

| イベント属性 | 説明                                   |
| ------------ | -------------------------------------- |
| :onclick     | クリックされた時                       |
| :ondblclick  | ダブルクリックされた時                 |
| :onmousedown | マウスのボタンが押し下げられた時       |
| :onmouseup   | マウスのボタンが離された時             |
| :onmouseover | カーソルが重なった時                   |
| :onmousemove | カーソルが移動した時                   |
| :onmouseout  | カーソルが離れた時                     |
| :onkeypress  | キーが押されて離された時               |
| :onkeydown   | キーが押し下げられた時                 |
| :onkeyup     | キーが離された時                       |
| :onfocus     | フォーカスされた時                     |
| :onblur      | フォーカスを失った時                   |
| :onselect    | 入力欄のテキストが選択された時         |
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### ラジオボタンOFF

    radio_button_tag 'page[category]', 'rails_base'
    #=> <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ラジオボタンON

    radio_button_tag 'page[category]', 'rails_base', true
    #=> <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### フォームの項目の利用禁止

    radio_button_tag 'page[category]', 'rails_base','', {disabled: true}
    #=> <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### Tabキーによる入力欄の移動順

    radio_button_tag 'page[category]', 'rails_base','', {tabindex: 1}
    #=> <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" />

#### フォームに移動するショートカットキー

    radio_button_tag 'page[category]', 'rails_base','', {accesskey: 'k'}
    #=> <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### class名を指定

    radio_button_tag 'color', "green", true, class: "color_input"
    #=> <input checked="checked" class="color_input" id="color_green" name="color" type="radio" value="green" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_tag_helper.rb#L469)

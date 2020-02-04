---
layout: page
---
### 使い方
    label_tag(要素名 [, ラベル配下のコンテンツ] [, HTML属性 or イベント属性])

### HTML属性

HTML属性      | 説明
---------- | ------------------
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
#### ラベル配下のコンテンツなし
    label_tag 'page[name]'
    # <label for="page_name">Name</label>

#### ラベル配下のコンテンツあり
    # @page.name = "abc"
    label_tag 'page[name]', @page.name
    # <label for="page_name">abc</label>

#### class属性の指定
    label_tag 'page[name]', '', class: 'page_name'
    # <label class="page_name" for="page_name">Name</label>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L215)
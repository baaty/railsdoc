---
layout: page
---
### 説明
隠しフィールドの生成

### 使い方
    hidden_field(オブジェクト名, メソッド名 [, HTML属性 or イベント属性])

#### f.object
    f.hidden_field(メソッド名 [, HTML属性 or イベント属性]

### HTML属性

HTML属性      | 説明
---------- | ------------------
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
#### hidden_field
##### 隠しフィールドの生成
    hidden_field :page, :set
    # <input id="page_set" name="page[set]" type="hidden" />

##### 初期値あり
    # @page.set = "abc"
    hidden_field :page, :set
    # <input id="page_set" name="page[set]" type="hidden" value="abc" />

##### class属性を指定
    hidden_field :page, :set, :class = 'set'
    # <input class='set' id="page_set" name="page[set]" type="hidden" />

#### f.hidden_field
##### 隠しフィールドの生成
    <%= f.hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" />

##### 初期値あり
    # @page.set = "abc"
    <%= hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" value="abc" />

##### class属性を指定
    <%= hidden_field :page, :set, :class = 'set' %>
    # <input class='set' id="page_set" name="page[set]" type="hidden" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1180)
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2357)
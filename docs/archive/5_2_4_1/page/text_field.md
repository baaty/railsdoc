---
layout: archive_page
---
### 説明
テキストボックスを生成

### 使い方
    text_field(オブジェクト名, メソッド名 [, HTML属性 or イベント属性])

### HTML属性

HTML属性   | 説明
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

### 例
#### テキストボックスを生成
    text_field :page, :name
    # <input id="page_name" name="page[name]" size="30" type="text" />

#### 初期値あり
    text_field :page, :name
    # <input id="page_name" name="page[name]" size="30" type="text" value="abc" />

#### class属性を指定
    text_field :page, :name, :class = 'page_name'
    # <input class="page_name" id="page_name" name="page[name]" size="30" type="text" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_helper.rb#L1135)
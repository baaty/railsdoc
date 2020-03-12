---
layout: archive_page
---
### 説明
モデルと関連のないチェックボックスを生成

### 使い方
    check_box_tag(要素名 [, value値, checked = false, オプション or HTML属性 or イベント属性])

### オプション

オプション   | 説明
---------- | ------------------
:disabled  | 無効化

### HTML属性

オプション   | 説明
---------- | ------------------
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
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
#### チェックボックスOFF
    check_box_tag 'page[freezeflag]', true, false, {}
    # <input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### チェックボックスON
    check_box_tag 'page[freezeflag]', true, true, {}
    # <input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### 利用禁止
    check_box_tag 'page[freezeflag]', true, false, {disabled: true}
    # <input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### Tabキーによる入力欄の移動順
    check_box_tag 'page[freezeflag]', true, false, {tabindex: 1}
    # <input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

#### フォームに移動するショートカットキー
    check_box_tag 'page[freezeflag]', true, false, {accesskey: 'k'}
    # <input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_tag_helper.rb#L378)
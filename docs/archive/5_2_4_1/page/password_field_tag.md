---
layout: archive_page
---
### 説明
モデルと関連のないパスワード入力ボックスを生成

### 使い方
    password_field_tag(要素名 [, value値, オプション or HTML属性 or イベント属性])

### オプション

オプション   | 説明
---------- | ------------------
:disabled  | 無効化
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数

### HTML属性

HTML属性   | 説明
---------- | ------------------
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
#### パスワード入力ボックスを生成
    password_field_tag 'pass'
    # <input id="pass" name="pass" type="password" />

##### value値を指定
    password_field_tag 'secret', 'Your secret here'
    # <input id="secret" name="secret" type="password" value="Your secret here" />

#### class属性を付与
    password_field_tag 'masked', nil, class: 'masked_input_field'
    # <input class="masked_input_field" id="masked" name="masked" type="password" />

#### フォーム幅を指定
    password_field_tag 'token', '', size: 15
    # <input id="token" name="token" size="15" type="password" value="" />

#### 入力可能な最大文字数
    password_field_tag 'key', nil, maxlength: 16
    # <input id="key" maxlength="16" name="key" type="password" />

#### 無効化
    password_field_tag 'confirm_pass', nil, disabled: true
    # <input disabled="disabled" id="confirm_pass" name="confirm_pass" type="password" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_tag_helper.rb#L311)
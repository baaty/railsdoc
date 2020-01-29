---
layout: page
---
### 使い方
    password_field_tag(要素名 [, 値, オプション or HTMLオプション])

### オプション

オプション   | 説明
---------- | ------------------
:disabled  | 無効化
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数

### HTMLオプション

オプション   | 説明
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

### 例
    password_field_tag 'pass'
    # <input id="pass" name="pass" type="password" />

    password_field_tag 'secret', 'Your secret here'
    # <input id="secret" name="secret" type="password" value="Your secret here" />

    password_field_tag 'masked', nil, class: 'masked_input_field'
    # <input class="masked_input_field" id="masked" name="masked" type="password" />

    password_field_tag 'token', '', size: 15
    # <input id="token" name="token" size="15" type="password" value="" />

    password_field_tag 'key', nil, maxlength: 16
    # <input id="key" maxlength="16" name="key" type="password" />

    password_field_tag 'confirm_pass', nil, disabled: true
    # <input disabled="disabled" id="confirm_pass" name="confirm_pass" type="password" />

    password_field_tag 'pin', '1234', maxlength: 4, size: 6, class: "pin_input"
    # <input class="pin_input" id="pin" maxlength="4" name="pin" size="6" type="password" value="1234" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L314)
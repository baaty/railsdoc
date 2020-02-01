---
layout: page
---
### radio_button
#### 説明
ラジオボタンを生成

#### 使い方
    radio_button(オブジェクト名, メソッド名, value値 [, オプション])

#### オプション

オプション   | 説明
---------- | ------------------
:checked   | チェックの有無
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

#### 例
##### ラジオボタンOFF
    radio_button 'page', 'category', 'rails_base'
    # <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### ラジオボタンON
    radio_button 'page', 'category', 'rails_base', checked: true
    # <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### フォームの項目の利用禁止
    radio_button 'page', 'category', 'rails_base', disabled: true
    # <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### Tabキーによる入力欄の移動順
    radio_button 'page', 'category', 'rails_base', tabindex: 1
    # <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" />

##### フォームに移動するショートカットキー
    radio_button 'page', 'category', 'rails_base', accesskey: 'k'
    # <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1322)

### f.radio_button
#### 説明
ラジオボタンを生成

#### 使い方
    f.radio_button(メソッド名, value値 [, オプション])

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックの有無
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

#### 例
##### ラジオボタンOFF
    f.radio_button 'category', 'rails_base'
    # <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### ラジオボタンON
    f.radio_button 'category', 'rails_base', checked: true
    # <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### フォームの項目の利用禁止
    f.radio_button 'category', 'rails_base', disabled: true
    # <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

##### Tabキーによる入力欄の移動順
    f.radio_button 'category', 'rails_base', tabindex: 1
    # <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" />

##### フォームに移動するショートカットキー
    f.radio_button 'category', 'rails_base', accesskey: 'k'
    # <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2335)
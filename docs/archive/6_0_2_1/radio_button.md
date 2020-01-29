---
layout: page
---
### radio_button
#### 説明
ラジオボックスを生成

#### 使い方
    radio_button(オブジェクト名, メソッド名, 値 [, オプション])

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
##### ラジオボックスOFF
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### ラジオボックスON
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {checked: true} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### フォームの項目の利用禁止
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {disabled: true} %><br />
    Rubeの基礎知識: <%= radio_button page', 'category', 'ruby_base', {disabled: true} %>
    # Railsの基礎知識: <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input disabled="disabled" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### Tabキーによる入力欄の移動順
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {tabindex: 1} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {tabindex: 2} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" tabindex="2" type="radio" value="ruby_base" />

##### フォームに移動するショートカットキー
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {accesskey: 'k'} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {accesskey: 'l'} %>
    # Railsの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1322)

### f.radio_button
#### 説明
ラジオボックスを生成

#### 使い方
    f.radio_button(メソッド名, 値 [, オプション])

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
##### ラジオボックスOFF
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### ラジオボックスON
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {checked: true} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### フォームの項目の利用禁止
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {disabled: true} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {disabled: true} %>
    # Railsの基礎知識: <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input disabled="disabled" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### Tabキーによる入力欄の移動順
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {tabindex: 1} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {tabindex: 2} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" tabindex="2" type="radio" value="ruby_base" />

##### フォームに移動するショートカットキー
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {accesskey: 'k'} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {accesskey: 'l'} %>
    # Railsの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2335)
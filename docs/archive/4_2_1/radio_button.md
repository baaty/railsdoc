---
layout: page
---
### radio_button
#### 説明
ラジオボックスを生成

#### 使い方
    radio_button(オブジェクト名, プロパティ名, 値 [, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックの有無
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:disabled  | フォームの項目の利用禁止
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
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {:checked => true} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### フォームの項目の利用禁止
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {:disabled => true} %><br />
    Rubeの基礎知識: <%= radio_button page', 'category', 'ruby_base', {:disabled => true} %>
    # Railsの基礎知識: <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input disabled="disabled" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### Tabキーによる入力欄の移動順
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {:tabindex => 1} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {:tabindex => 2} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" tabindex="2" type="radio" value="ruby_base" />

##### フォームに移動するショートカットキー
    Railsの基礎知識: <%= radio_button 'page', 'category', 'rails_base', {:accesskey => 'k'} %><br />
    Rubeの基礎知識: <%= radio_button 'page', 'category', 'ruby_base', {:accesskey => 'l'} %>
    # Railsの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L966)

### f.radio_button
#### 説明
ラジオボックスを生成

#### 使い方
    f.radio_button(プロパティ名, 値 [, オプション])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックの有無
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:disabled  | フォームの項目の利用禁止
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
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {:checked => true} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {} %>
    # Railsの基礎知識: <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### フォームの項目の利用禁止
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {:disabled => true} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {:disabled => true} %>
    # Railsの基礎知識: <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input disabled="disabled" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

##### Tabキーによる入力欄の移動順
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {:tabindex => 1} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {:tabindex => 2} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" tabindex="2" type="radio" value="ruby_base" />

##### フォームに移動するショートカットキー
    Railsの基礎知識: <%= f.radio_button 'category', 'rails_base', {:accesskey => 'k'} %><br />
    Rubeの基礎知識: <%= f.radio_button 'category', 'ruby_base', {:accesskey => 'l'} %>
    # Railsの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1729)

### radio_buttonとradio_button_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
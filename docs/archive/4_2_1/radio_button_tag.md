---
layout: page
---
### 使い方
    radio_button_tag(要素名, 値 [, checked = false, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション      | 説明
---------- | ------------------
:disabled  | フォームの項目の利用禁止
:checked   | チェックの有無
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

### 例
#### ラジオボックスOFF
    Railsの基礎知識: <%= radio_button_tag 'page[category]', 'rails_base' %><br />
    Rubeの基礎知識: <%= radio_button_tag 'page[category]', 'ruby_base' %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

#### ラジオボックスON
    Railsの基礎知識: <%= radio_button_tag 'page[category]', 'rails_base' %><br />
    Rubeの基礎知識: <%= radio_button_tag 'page[category]', 'ruby_base' %>
    # Railsの基礎知識: <input checked="checked" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input checked="checked" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

#### フォームの項目の利用禁止
    Railsの基礎知識: <%= radio_button_tag 'page[category]', 'rails_base','', {:disabled => true} %><br />
    Rubeの基礎知識: <%= radio_button_tag 'page[category]', 'ruby_base','', {:disabled => true} %>
    # Railsの基礎知識: <input disabled="disabled" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input disabled="disabled" id="page_category_ruby_base" name="page[category]" type="radio" value="ruby_base" />

#### Tabキーによる入力欄の移動順
    Railsの基礎知識: <%= radio_button_tag 'page[category]', 'rails_base','', {:tabindex => 1} %><br />
    Rubeの基礎知識: <%= radio_button_tag 'page[category]', 'ruby_base','', {:tabindex => 2} %>
    # Railsの基礎知識: <input id="page_category_rails_base" name="page[category]" tabindex="1" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input id="page_category_ruby_base" name="page[category]" tabindex="2" type="radio" value="ruby_base" />

#### フォームに移動するショートカットキー
    Railsの基礎知識: <%= radio_button_tag 'page[category]', 'rails_base','', {:accesskey => 'k'} %><br />
    Rubeの基礎知識: < %= radio_button_tag 'page[category]', 'ruby_base','', {:accesskey => 'l'} %>
    # Railsの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" /><br />
    # Rubeの基礎知識: <input accesskey="k" id="page_category_rails_base" name="page[category]" type="radio" value="rails_base" />

### ソースコード
* [Search: radio_button_tag - GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L397>GitHub</a></li></ul>
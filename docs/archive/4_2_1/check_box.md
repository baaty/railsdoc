---
layout: page
---
### check_box
#### 説明
チェックボックスを生成

#### 使い方
    check_box(オブジェクト名, プロパティ名 [, オプション, checked_value = "1", unchecked_value = "0"])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックボックスのチェックの有無
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
##### チェックボックスOFF
    <%= check_box 'page', 'freezeflag', {}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### チェックボックスON
    <%= check_box 'page', 'freezeflag', {:checked => true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### 利用禁止
    <%= check_box 'page', 'freezeflag', {:disabled => true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### Tabキーによる入力欄の移動順
    <%= check_box 'page', 'freezeflag', {:tabindex => 1}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

##### フォームに移動するショートカットキー
    <%= check_box 'page', 'freezeflag', {:accesskey => 'k'}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />


#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L945)

### f.check_box
#### 説明
チェックボックスを生成

#### 使い方
    f.check_box(プロパティ名 [, オプション, checked_value = "1", unchecked_value = "0"])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックボックスのチェックの有無
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
##### チェックボックスOFF
    <%= f.check_box 'freezeflag', {}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### チェックボックスON
    <%= f.check_box 'freezeflag', {:checked => true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### 利用禁止
    <%= f.check_box 'freezeflag', {:disabled => true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### Tabキーによる入力欄の移動順
    <%= f.check_box 'freezeflag', {:tabindex => 1}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

##### フォームに移動するショートカットキー
    <%= f.check_box 'freezeflag', {:accesskey => 'k'}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1708)


### check_boxとcheck_box_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
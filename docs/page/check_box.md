---
layout: page
---
### check_box
#### 説明
チェックボックスを生成

#### 使い方
    check_box(オブジェクト名, メソッド名 [, オプション, checked_value = "1", unchecked_value = "0"])

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックボックスのチェックの有無
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
##### チェックボックスOFF
    <%= check_box 'page', 'freezeflag', {}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### チェックボックスON
    <%= check_box 'page', 'freezeflag', {checked: true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### 利用禁止
    <%= check_box 'page', 'freezeflag', {disabled: true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### Tabキーによる入力欄の移動順
    <%= check_box 'page', 'freezeflag', {tabindex: 1}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

##### フォームに移動するショートカットキー
    <%= check_box 'page', 'freezeflag', {accesskey: 'k'}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />


#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1300)

### f.check_box
#### 説明
チェックボックスを生成

#### 使い方
    f.check_box(メソッド名 [, オプション, checked_value = "1", unchecked_value = "0"])

#### オプション

オプション      | 説明
---------- | ------------------
:checked   | チェックボックスのチェックの有無
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
##### チェックボックスOFF
    <%= f.check_box 'freezeflag', {}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### チェックボックスON
    <%= f.check_box 'freezeflag', {checked: true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### 利用禁止
    <%= f.check_box 'freezeflag', {disabled: true}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

##### Tabキーによる入力欄の移動順
    <%= f.check_box 'freezeflag', {tabindex: 1}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

##### フォームに移動するショートカットキー
    <%= f.check_box 'freezeflag', {accesskey: 'k'}, true, false %>
    # <input name="page[freezeflag]" type="hidden" value="false" /><input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2313)
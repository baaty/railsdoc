---
layout: page
---
### 説明
チェックボックスを生成

### 使い方
    check_box_tag(要素名 [, 値, checked = false, オプション or HTMLオプション])

### オプション

オプション   | 説明
---------- | ------------------
:disabled  | 無効化

### HTMLオプション

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

### 例
#### チェックボックスOFF
    <%= check_box_tag 'page[freezeflag]', true, false, {} %>
    # <input id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### チェックボックスON
    <%= check_box_tag 'page[freezeflag]', true, true, {} %>
    # <input checked="checked" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### 利用禁止
    <%= check_box_tag 'page[freezeflag]', true, false, {disabled: true} %>
    # <input disabled="disabled" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

#### Tabキーによる入力欄の移動順
    <%= check_box_tag 'page[freezeflag]', true, false, {tabindex: 1} %>
    # <input id="page_freezeflag" name="page[freezeflag]" tabindex="1" type="checkbox" value="true" />

#### フォームに移動するショートカットキー
    <%= check_box_tag 'page[freezeflag]', true, false, {accesskey: 'k'} %>
    # <input accesskey="k" id="page_freezeflag" name="page[freezeflag]" type="checkbox" value="true" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L381)
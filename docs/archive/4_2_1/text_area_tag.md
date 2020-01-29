---
layout: page
---
### 使い方
    text_area_tag(要素名 [, エリア配下のテキスト, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション      | 説明
---------- | ------------------
:size      | フォームの幅
:rows      | rowsの設定
:cols      | columnsの設定
:disabled  | フォームの項目の利用禁止
:escape    | HTMLをエスケープするか
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
#### 基本形(オプションなし)
    <%= text_area_tag 'page[comtent]' %>
    # <textarea id="page_content" name="page[content]"></textarea>

#### 初期値あり
    # @page.comtent = "初期値"
    <%= text_area_tag 'page[comtent]', @page.comtent %>
    # <textarea id="page_content" name="page[content]">初期値</textarea>

#### フォームの幅(20x10)
    <%= text_area_tag 'page[comtent]', '', :size => "20x10" %>
    # <textarea cols="20" id="page_content" name="page[content]" rows="10"></textarea>

#### 入力フィールドに入力可能な最大文字数
    <%= text_area_tag :'age[comtent]', '', :maxlength => "20" %>
    # <textarea id="page_content" maxlength="20" name="page[content]"></textarea>

#### フォームの項目の利用禁止
    <%= text_area_tag 'page[comtent]', '', :maxlength => "20" %>
    # <textarea disabled ="disabled" id="page_content" name="page[content]"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L338)
---
layout: page
---
### text_area
#### 説明
テキストエリアを生成

#### 使い方
    text_area(オブジェクト名, メソッド名 [, HTML属性 or イベント属性])

#### HTML属性

HTML属性   | 説明
---------- | ------------------
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

#### 例
##### 基本形(オプションなし)
    <%= text_area :page, :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20"></textarea>

##### 初期値あり
    # @page.comtent = "初期値"
    <%= text_area :page, :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20">初期値</textarea>

##### フォームの幅(20x10)
    <%= text_area :page, :comtent, size: "20x10" %>
    # <textarea cols="20" id="page_content" name="page[content]" rows="10"></textarea>

##### 入力フィールドに入力可能な最大文字数
    <%= text_area :page, :comtent, maxlength: "20" %>
    # <textarea cols="40" id="page_content" maxlength="20" name="page[content]" rows="20"></textarea>

##### フォームの項目の利用禁止
    <%= text_area :page, :comtent, maxlength: "20" %>
    # <textarea cols="40" disabled ="disabled" id="page_content" name="page[content]" rows="20"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1240)

### f.text_area
#### 説明
テキストエリアを生成

#### 使い方
    f.text_area(メソッド名 [, オプション])

#### オプション

オプション      | 説明
---------- | ------------------
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
##### 基本形(オプションなし)
    <%= f.text_area :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20"></textarea>

##### 初期値あり
    # @page.comtent = "初期値"
    <%= f.text_area :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20">初期値</textarea>

##### フォームの幅(20x10)
    <%= f.text_area :comtent, size: "20x10" %>
    # <textarea cols="20" id="page_content" name="page[content]" rows="10"></textarea>

##### 入力フィールドに入力可能な最大文字数
    <%= f.text_area :comtent, maxlength: "20" %>
    # <textarea cols="40" id="page_content" maxlength="20" name="p>ge[content]" rows="20"></textarea>

##### フォームの項目の利用禁止
    <%= f.text_area :comtent, maxlength: "20" %>
    # <textarea cols="40" disabled ="disabled" id="page_content" name="page[content]" rows="20"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1722)
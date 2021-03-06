---
layout: page
---
### text_area
#### 説明
テキストエリアを生成

#### 使い方
    text_area(オブジェクト名, プロパティ名 [, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
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
##### 基本形(オプションなし)
    <%= text_area :page, :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20"></textarea>

##### 初期値あり
    # @page.comtent = "初期値"
    <%= text_area :page, :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20">初期値</textarea>

##### フォームの幅(20x10)
    <%= text_area :page, :comtent, :size => "20x10" %>
    # <textarea cols="20" id="page_content" name="page[content]" rows="10"></textarea>

##### 入力フィールドに入力可能な最大文字数
    <%= text_area :page, :comtent, :maxlength => "20" %>
    # <textarea cols="40" id="page_content" maxlength="20" name="page[content]" rows="20"></textarea>

##### フォームの項目の利用禁止
    <%= text_area :page, :comtent, :maxlength => "20" %>
    # <textarea cols="40" disabled ="disabled" id="page_content" name="page[content]" rows="20"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L885)

### f.text_area
#### 説明
テキストエリアを生成

#### 使い方
    f.text_area(プロパティ名 [, オプション])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション      | 説明
---------- | ------------------
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
##### 基本形(オプションなし)
    <%= f.text_area :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20"></textarea>

##### 初期値あり
    # @page.comtent = "初期値"
    <%= f.text_area :comtent %>
    # <textarea cols="40" id="page_content" name="page[content]" rows="20">初期値</textarea>

##### フォームの幅(20x10)
    <%= f.text_area :comtent, :size => "20x10" %>
    # <textarea cols="20" id="page_content" name="page[content]" rows="10"></textarea>

##### 入力フィールドに入力可能な最大文字数
    <%= f.text_area :comtent, :maxlength => "20" %>
    # <textarea cols="40" id="page_content" maxlength="20" name="p>ge[content]" rows="20"></textarea>

##### フォームの項目の利用禁止
    <%= f.text_area :comtent, :maxlength => "20" %>
    # <textarea cols="40" disabled ="disabled" id="page_content" name="page[content]" rows="20"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L885)

### text_areaとtext_area_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
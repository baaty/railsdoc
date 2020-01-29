---
layout: page
---
### text_field
#### 説明
テキストボックスを生成

#### 使い方
    text_field(オブジェクト名, プロパティ名 [, オプション])

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
##### 初期値なし
    <%= text_field :page, :name %>
    # <input id="page_name" name="page[name]" size="30" type="text" />

##### 初期値あり
    # @page.name = "abc"
    <%= text_field :page, :name %>
    # <input id="page_name" name="page[name]" size="30" type="text" value="abc" />

##### class属性を指定
    <%= text_field :page, :name, :class = 'page_name' %>
    # <input class="page_name" id="page_name" name="page[name]" size="30" type="text" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L786)

### f.text_field
#### 説明
テキストボックスを生成

#### 使い方
    f.text_field(プロパティ名 [, オプション])

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
##### 初期値なし
    <%= f.text_field :name %>
    # <input id="page_name" name="page[name]" size="30" type="text" />

##### 初期値あり
    # @page.name = "abc"
    <%= f.text_field :name %>
    # <input id="page_name" name="page[name]" size="30" type="text" value="abc" />

##### class属性を指定
    <%= f.text_field :name, :class = 'page_name' %>
    # <input class="page_name" id="page_name" name="page[name]" size="30" type="text" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L786)

### text_fieldとtext_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
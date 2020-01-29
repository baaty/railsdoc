---
layout: page
---
### label
#### 説明
指定されたモデルに対して、labelタグを生成する

#### 使い方

    label(オブジェクト名, プロパティ名 [, ラベル配下のコンテンツ] [, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
##### ラベル配下のコンテンツなし
    <%= label :page, :name %>
    # <label for="page_name">Name</label>

##### ラベル配下のコンテンツあり
    # @page.name = "abc"
    <%= label :page, :name, @page.name %>
    # <label for="page_name">abc</label>

##### class属性の指定
    <%= label :page, :name, '', :class = 'page_name' %>
    # <label class="page_name" for="page_name">Name</label>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L765)

### f.label
#### 説明
指定されたモデルに対して、labelタグを生成する

#### 使い方
    f.label(プロパティ名 [, ラベル配下のコンテンツ] [, オプション])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション      | 説明
---------- | ------------------
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
##### ラベル配下のコンテンツなし
    <%= f.label :name %>
    # <label for="page_name">Name</label>

##### ラベル配下のコンテンツあり
    # @page.name = "abc"
    <%= f.label :name, @page.name %>
    # <label for="page_name">abc</label>

##### class属性の指定
    <%= f.label :name, '', :class = 'page_name' %>
    # <label class="page_name" for="page_name">Name</label>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1648)

### labelとlabel_tagの違い
* POSTパラメータがハッシュ形式
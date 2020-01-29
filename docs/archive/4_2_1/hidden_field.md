---
layout: page
---
### hidden_field
#### 説明
隠しフィールドの生成

#### 使い方
    hidden_field(オブジェクト名, プロパティ名 [, オプション])

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
    <%= hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" />

##### 初期値あり
    # @page.set = "abc"
    <%= hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" value="abc" />

##### class属性を指定
    <%= hidden_field :page, :set, :class = 'set' %>
    # <input class='set' id="page_set" name="page[set]" type="hidden" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L825)

### f.hidden_field
#### 説明
隠しフィールドの生成

#### 使い方
    f.hidden_field(プロパティ名 [, オプション]

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
    <%= hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" />

##### 初期値あり
    # @page.set = "abc"
    <%= hidden_field :page, :set %>
    # <input id="page_set" name="page[set]" type="hidden" value="abc" />

##### class属性を指定
    <%= hidden_field :page, :set, :class = 'set' %>
    # <input class='set' id="page_set" name="page[set]" type="hidden" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1748)

### hidden_fieldとhidden_field_tagの違い
* POSTパラメータがハッシュ形式
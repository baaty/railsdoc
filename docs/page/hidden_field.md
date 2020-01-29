---
layout: page
---
### hidden_field
#### 説明
隠しフィールドの生成

#### 使い方
    hidden_field(オブジェクト名, メソッド名 [, HTMLオプション])

#### HTMLオプション

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1180)

### f.hidden_field
#### 説明
隠しフィールドの生成

#### 使い方
    f.hidden_field(メソッド名 [, HTMLオプション]

#### HTMLオプション

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2357)
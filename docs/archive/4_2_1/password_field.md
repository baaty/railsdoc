---
layout: page
---
### password_field
#### 説明
パスワード入力ボックスを生成

#### 使い方
    password_field(オブジェクト名, プロパティ名 [, オプション])

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
    <%= password_field :page, :pass %>
    # <input id="page_pass" name="page[pass]" size="30" type="password" />

##### 初期値あり
    # @page.pass = "abc"
    <%= password_field :page, :pass %>
    # <input id="page_pass" name="page[pass]" size="30" type="password" value="abc" />

##### フォームの幅
    <%= password_field :page, :pass, :size = '40' %>
    # <input id="page_pass" name="page[pass]" size="40" type="password" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L807)

### f.password_field
#### 説明
パスワード入力ボックスを生成

#### 使い方
    f.password_field(プロパティ名 [, オプション])

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
    <%= f.password_field :pass %>
    # <input id="page_pass" name="page[pass]" size="30" type="password" />

##### 初期値あり
    # @page.pass = "abc"
    <%= f.password_field :pass %>
    # <input id="page_pass" name="page[pass]" size="30" type="password" value="abc" />

##### フォームの幅
    <%= f.password_field :pass, :size = '40' %>
    # <input id="page_pass" name="page[pass]" size="40" type="password" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L807)

### password_firldとpassword_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
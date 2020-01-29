---
layout: page
---
### file_field
#### 説明
ファイル選択ボックスを生成

#### 使い方
    file_field(オブジェクト名, プロパティ名 [, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション      | 説明
---------- | ------------------
:disabled  | フォームの項目の利用禁止
:accept    | フォームで受付可能なMIMEタイプ
:multiple  | 複数選択可能
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

#### 例
##### オプションなし
    <%= file_field :page, :fine_name %>
    # <input id="page_fine_name" name="page[fine_name]" size="30" type="file" />

##### class属性を指定
    <%= file_field :page, :fine_name, :class = 'page_fine_name' %>
    # <input class="page_fine_name" id="page_fine_name" name="page[fine_name]" size="30" type="file" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L857)

### f.file_field
#### 説明
ファイル選択ボックスを生成

#### 使い方
    f.file_field(プロパティ名 [, オプション])

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
##### オプションなし
    <%= f.file_field :fine_name %>
    # <input id="page_fine_name" name="page[fine_name]" size="30" type="file" />

##### class属性を指定
    <%= f.file_field :fine_name, :class = 'page_fine_name' %>
    # <input class="page_fine_name" id="page_fine_name" name="page[fine_name]" size="30" type="file" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1781)

### file_fieldとfile_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
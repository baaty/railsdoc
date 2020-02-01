---
layout: page
---
### file_field
#### 説明
ファイル選択ボックスを生成

#### 使い方
    file_field(オブジェクト名, メソッド名 [, オプション])

#### オプション

オプション      | 説明
---------- | ------------------
:disabled  | 無効化
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
:value     | 初期値

#### 例
##### オプションなし
    <%= file_field :page, :fine_name %>
    # <input id="page_fine_name" name="page[fine_name]" size="30" type="file" />

##### class属性を指定
    <%= file_field :page, :fine_name, :class = 'page_fine_name' %>
    # <input class="page_fine_name" id="page_fine_name" name="page[fine_name]" size="30" type="file" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2395)

### f.file_field
#### 説明
ファイル選択ボックスを生成

#### 使い方
    f.file_field(メソッド名 [, オプション])

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
:value     | 初期値

#### 例
##### オプションなし
    <%= f.file_field :fine_name %>
    # <input id="page_fine_name" name="page[fine_name]" size="30" type="file" />

##### class属性を指定
    <%= f.file_field :fine_name, :class = 'page_fine_name' %>
    # <input class="page_fine_name" id="page_fine_name" name="page[fine_name]" size="30" type="file" />
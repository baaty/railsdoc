---
layout: page
---
### search_field
#### 説明
検索ボックスを生成

#### 使い方
    search_field(オブジェクト名, プロパティ名 [, オプション])

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
    search_field(:user, :name)
    # => <input id="user_name" name="user[name]" type="search" />
    search_field(:user, :name, autosave: false)
    # => <input autosave="false" id="user_name" name="user[name]" type="search" />
    search_field(:user, :name, results: 3)
    # => <input id="user_name" name="user[name]" results="3" type="search" />
    #  Assume request.host returns "www.example.com"
    search_field(:user, :name, autosave: true)
    # => <input autosave="com.example.www" id="user_name" name="user[name]" results="10" type="search" />
    search_field(:user, :name, onsearch: true)
    # => <input id="user_name" incremental="true" name="user[name]" onsearch="true" type="search" />
    search_field(:user, :name, autosave: false, onsearch: true)
    # => <input autosave="false" id="user_name" incremental="true" name="user[name]" onsearch="true" type="search" />
    search_field(:user, :name, autosave: true, onsearch: true)
    # => <input autosave="com.example.www" id="user_name" incremental="true" name="user[name]" onsearch="true" results="10" type="search" />

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L997)

### f.search_field
#### 説明
検索ボックスを生成

#### 使い方
    f.search_field(プロパティ名 [, オプション])

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

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L997)

### search_fieldとsearch_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式
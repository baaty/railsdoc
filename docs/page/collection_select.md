---
layout: page
---
### collection_select
#### 説明
選択ボックスをモデルの情報を元に生成

#### 使い方
    collection_select(オブジェクト名, メソッド名, 要素の配列, value属性の項目, テキストの項目 [, オプション or HTMLオプション])

#### オプション

オプション          | 説明
---------------|--------------
:include_blank | 空のオプションを先頭に追加
:disabled      | 無効化
:selected      | 選択されたオプション

#### HTMLオプション

オプション      | 説明
-----------|-------------------
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
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
    <%= collection_select(:page, :name, @categories, :id, :name) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 空のオプションを先頭に追加
    <%= collection_select(:page, :name, @categories, :id, :name, nil, prompt: "選択してください") %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 空のオプションを先頭に追加
    <%= collection_select(:page, :name, @categories, :id, :name, include_blank: true) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 選択されたオプション
    <%= collection_select(:page, :name, @categories, :id, :name, selected: 2) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2" selected="selected">Rubyの基礎知識</option>
    # </select>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L203)

### f.collection_select
#### 説明
選択ボックスをモデルの情報を元に生成

#### 使い方
    f.collection_select(メソッド名, オブジェクトの配列, value属性の項目, テキストの項目 [, オプション or HTMLオプション])

#### オプション

オプション          | 説明
---------------|--------------
:include_blank | 空のオプションを先頭に追加
:disabled      | 無効化
:selected      | 選択されたオプション

#### HTMLオプション

オプション      | 説明
-----------|-------------------
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
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
    <%= f.collection_select(:name, @categories, :id, :name) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 空のオプションを先頭に追加
    <%= f.collection_select(:name, @categories, :id, :name, nil, prompt: "選択してください") %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 空のオプションを先頭に追加
    <%= f.collection_select(:name, @categories, :id, :name, include_blank: true) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2">Rubyの基礎知識</option>
    # </select>

##### 選択されたオプション
    <%= f.collection_select(:name, @categories, :id, :name, selected: 2) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option>
    # <option value="2" selected="selected">Rubyの基礎知識</option>
    # </select>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L843)
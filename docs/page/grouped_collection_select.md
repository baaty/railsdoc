---
layout: page
---
### grouped_collection_select
#### 説明
選択ボックスをグループ化

#### 使い方
    grouped_collection_select(オブジェクト名, メソッド名, オブジェクトの配列, タグを取得するメソッド, タグのラベル, valueの項目, テキストの項目 [, オプション or HTML属性 or イベント属性])

#### オプション

オプション          | 説明
-------------- | ---------------
:include_blank | 空のオプションを先頭に追加
:prompt        | 指定したオプションを先頭に追加
:selected      | 選択されたオプション

### HTML属性

HTML属性      | 説明
-----------|------------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | 移動するショートカットキー
:usemap    | この画像に対応させるイメージマップ
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時
:onchange    | フォーカスを失う際に値が変化していた時

#### 例
##### オプションなし
    # @categories = Category.all
    <%= grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name) %>
    # <select id="page_name" name="page[name]"><optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 空のオプションを先頭に追加
    # @categories = Category.all
    <%= grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name, include_blank: true) %>
    # <select id="page_name" name="page[name]"><option value=""></option>
    # <optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 指定したオプションを先頭に追加
    # @categories = Category.all
    <%= grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name, :prompt = "選択してください") %>
    # <select id="page_name" name="page[name]"><option value="">選択してください</option>
    # <optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 選択したオプション
    # @categories = Category.all
    # @page.name = 2
    <%= grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name) %>
    # <select id="page_name" name="page[name]"><optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2" selected="selected">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L263)

### f.grouped_collection_select
#### 説明
選択ボックスをグループ化

#### 使い方
    f.grouped_collection_select(メソッド名, オブジェクトの配列, タグを取得するメソッド, タグのラベル, valueの項目, テキストの項目 [, オプション or HTML属性 or イベント属性])

#### オプション

オプション          | 説明
-------------- | ---------------
:include_blank | 空のオプションを先頭に追加
:prompt        | 指定したオプションを先頭に追加
:selected      | 選択されたオプション

### HTML属性

HTML属性      | 説明
-----------|------------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | 移動するショートカットキー
:usemap    | この画像に対応させるイメージマップ
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

#### 例
##### オプションなし
    # @categories = Category.all
    <%= f.grouped_collection_select(:name, @categories, :pages, :name, :id, :name) %>
    # <select id="page_name" name="page[name]"><optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 空のオプションを先頭に追加
    # @categories = Category.all
    <%= f.grouped_collection_select(:name, @categories, :pages, :name, :id, :name, include_blank: true) %>
    # <select id="page_name" name="page[name]"><option value=""></option>
    # <optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 指定したオプションを先頭に追加
    # @categories = Category.all
    <%= f.grouped_collection_select(:name, @categories, :pages, :name, :id, :name, :prompt = "選択してください") %>
    # <select id="page_name" name="page[name]"><option value="">選択してください</option>
    # <optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

##### 選択したオプション
    # @categories = Category.all
    # @page.name = 2
    <%= f.grouped_collection_select(:name, @categories, :pages, :name, :id, :name) %>
    # <select id="page_name" name="page[name]"><optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2" selected="selected">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L855)
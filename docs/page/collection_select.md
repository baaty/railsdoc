---
layout: page
---

### 説明

選択ボックスをモデルの情報を元に生成

### 使い方

    collection_select(オブジェクト名, メソッド名, 要素の配列, value属性の項目, テキストの項目, オプション={}, HTML属性={} or イベント属性={})

    # f.object
    f.collection_select(メソッド名, 要素の配列, value属性の項目, テキストの項目, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション     | 説明                       |
| -------------- | -------------------------- |
| :include_blank | 空のオプションを先頭に追加 |
| :disabled      | 無効化                     |
| :selected      | 選択されたオプション       |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :size      | フォームの幅                         |
| :maxlength | 入力フィールドに入力可能な最大文字数 |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### イベント属性

| イベント属性 | 説明                                   |
| ------------ | -------------------------------------- |
| :onclick     | クリックされた時                       |
| :ondblclick  | ダブルクリックされた時                 |
| :onmousedown | マウスのボタンが押し下げられた時       |
| :onmouseup   | マウスのボタンが離された時             |
| :onmouseover | カーソルが重なった時                   |
| :onmousemove | カーソルが移動した時                   |
| :onmouseout  | カーソルが離れた時                     |
| :onkeypress  | キーが押されて離された時               |
| :onkeydown   | キーが押し下げられた時                 |
| :onkeyup     | キーが離された時                       |
| :onfocus     | フォーカスされた時                     |
| :onblur      | フォーカスを失った時                   |
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### 選択ボックスをモデルの情報を元に生成

    collection_select(:page, :name, @categories, :id, :name)
    #=> <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option><option value="2">Rubyの基礎知識</option></select>

#### 空のオプションを先頭に追加

    collection_select(:page, :name, @categories, :id, :name, nil, prompt: "選択してください")
    #=> <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option><option value="2">Rubyの基礎知識</option></select>

#### 空のオプションを先頭に追加

    collection_select(:page, :name, @categories, :id, :name, include_blank: true)
    #=> <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option><option value="2">Rubyの基礎知識</option></select>

#### 選択されたオプション

    collection_select(:page, :name, @categories, :id, :name, selected: 2)
    #=> <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option><option value="2" selected="selected">Rubyの基礎知識</option></select>

#### 選択ボックスをモデルの情報を元に生成(f.collection_select)

    f.collection_select(:name, @categories, :id, :name)
    #=> <select id="page_name" name="page[name]"><option value="1">Railsの基礎知識</option><option value="2">Rubyの基礎知識</option></select>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L198)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L857)

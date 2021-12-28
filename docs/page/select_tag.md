---
layout: page
---

### 説明

選択ボックスを生成

### 使い方

    select_tag(要素名, オプションタグ=nil, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション     | 説明                           | デフォルト値 |
| -------------- | ------------------------------ | ------------ |
| :multiple      | 複数選択を有効にするか         |              |
| :disabled      | 無効化                         | false        |
| :include_blank | 先頭に空の要素を追加するか     |              |
| :prompt        | 指定したオプションを先頭に追加 |              |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
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

#### 選択ボックスを生成

    select_tag "people", options_from_collection_for_select(@people, "id", "name")
    #=> <select id="people" name="people"><option value="1">David</option></select>

#### 選択済みオプションあり

    select_tag "people", options_from_collection_for_select(@people, "id", "name", "1")
    #=> <select id="people" name="people"><option value="1" selected="selected">David</option></select>

#### rawで直接指定

    select_tag "people", raw("<option>David</option>")
    #=> <select id="people" name="people"><option>David</option></select>

#### 複数選択を有効

    select_tag "colors", raw("<option>Red</option><option>Green</option><option>Blue</option>"), multiple: true
    #=> <select id="colors" multiple="multiple" name="colors[]"><option>Red</option><option>Green</option><option>Blue</option></select>

#### class属性など指定

    select_tag "access", raw("<option>Read</option><option>Write</option>"), multiple: true, class: 'form_input', id: 'unique_id'
    #=> <select class="form_input" id="unique_id" multiple="multiple" name="access[]"><option>Read</option><option>Write</option></select>

#### 先頭に空の要素を追加

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), include_blank: true
    #=> <select id="people" name="people"><option value="" label=" "></option><option value="1">David</option></select>

#### 先頭に指定した文字列を追加

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), include_blank: "All"
    #=> <select id="people" name="people"><option value="">All</option><option value="1">David</option></select>

#### 指定したオプションを先頭に追加

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), prompt: "Select something"
    #=> <select id="people" name="people"><option value="">Select something</option><option value="1">David</option></select>

#### 無効化

    select_tag "destination", raw("<option>NYC</option><option>Paris</option><option>Rome</option>"), disabled: true
    #=> <select disabled="disabled" id="destination" name="destination"><option>NYC</option><option>Paris</option><option>Rome</option></select>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_tag_helper.rb#L198)

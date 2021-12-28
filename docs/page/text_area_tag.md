---
layout: page
---

### 説明

モデルと関連のないテキストエリアを生成

### 使い方

    text_area_tag(要素名, エリア配下のテキスト, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション | 説明                   |
| ---------- | ---------------------- |
| :size      | フォームの幅           |
| :rows      | rowsの設定             |
| :cols      | columnsの設定          |
| :disabled  | 無効化                 |
| :escape    | HTMLをエスケープするか |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :maxlength | 入力フィールドに入力可能な最大文字数 |
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

| イベント属性 | 説明                             |
| ------------ | -------------------------------- |
| :onclick     | クリックされた時                 |
| :ondblclick  | ダブルクリックされた時           |
| :onmousedown | マウスのボタンが押し下げられた時 |
| :onmouseup   | マウスのボタンが離された時       |
| :onmouseover | カーソルが重なった時             |
| :onmousemove | カーソルが移動した時             |
| :onmouseout  | カーソルが離れた時               |
| :onkeypress  | キーが押されて離された時         |

### 例

#### テキストエリアを生成

    text_area_tag 'post'
    #=> <textarea id="post" name="post"></textarea>

#### テキストエリアに表示する文字列を指定

    text_area_tag 'bio', @user.bio
    #=> <textarea id="bio" name="bio">This is my biography.</textarea>

#### カラム数などを指定

    text_area_tag 'body', nil, rows: 10, cols: 25
    #=> <textarea cols="25" id="body" name="body" rows="10"></textarea>

#### フォーム幅を指定

    text_area_tag 'body', nil, size: "25x10"
    #=> <textarea name="body" id="body" cols="25" rows="10"></textarea>

#### 無効化

    text_area_tag 'description', "Description goes here.", disabled: true
    #=> <textarea disabled="disabled" id="description" name="description">Description goes here.</textarea>

#### class属性を指定

    text_area_tag 'comment', nil, class: 'comment_input'
    #=> <textarea class="comment_input" id="comment" name="comment"></textarea>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_tag_helper.rb#L410)

---
layout: page
---

### 説明

任意のHTMLタグを生成

### 使い方

    tag(タグ名=nil, オプション=nil or HTML属性=nil or イベント属性=nil, HTML4互換=false, エスケープするか=true)

### オプション

| オプション | 説明                   |
| ---------- | ---------------------- |
| :data      | Data要素のカスタマイズ |
| :disabled  | 無効化                 |

### HTML属性

| HTML属性      | 説明                                   |
| ------------- | -------------------------------------- |
| :confirm      | 確認ダイアログに表示する文字列         |
| :disable_with | ボタンを無効化したときに表示する文字列 |
| :size         | フォームの幅                           |
| :maxlength    | 入力フィールドに入力可能な最大文字数   |
| :accept       | フォームで受付可能なMIMEタイプ         |
| :readonly     | フォームの内容変更禁止                 |
| :tabindex     | Tabキーによる入力欄の移動順            |
| :accesskey    | フォームに移動するショートカットキー   |
| :id           | 要素固有の識別子                       |
| :class        | 要素を分類するクラス名                 |
| :title        | 要素の補足情報                         |
| :style        | 要素の補足情報                         |
| :dir          | 表記方向                               |
| :lang         | 基本言語                               |

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
| :onkeydown   | キーが押し下げられた時           |
| :onkeyup     | キーが離された時                 |

### 例

#### h1タグを生成

    tag.h1 'All titles fit to print'
    #=> <h1>All titles fit to print</h1>

#### divタグを生成

    tag.div tag.p('Hello world!')
    #=> <div><p>Hello world!</p></div>

#### class属性を複数指定

    tag.section class: %w( kitties puppies )
    #=> <section class="kitties puppies"></section>

#### sectionタグを生成

    tag.section id: dom_id(@post)
    #=> <section id="<generated dom id>"></section>

#### 無効化

    tag.input type: 'text', disabled: true
    #=> <input type="text" disabled="disabled">

#### data属性を指定

    tag.article data: { user_id: 123 }
    #=> <article data-user-id="123"></article>

#### 古い指定の仕方

    tag(name, options = nil, open = false, escape = true)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/tag_helper.rb#L299)

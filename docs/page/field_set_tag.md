---
layout: page
---

### 説明

モデルを固定してフォームを生成  
form_for内で異なるモデルを編集できるようになる

### 使い方

    field_set_tag(サブフォームのタイトル=nil, HTML属性=nil or イベント属性=nil, ブロック引数)

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
| :onselect    | 入力欄のテキストが選択された時         |
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### モデルを固定してフォームを生成 

    <%= field_set_tag do %>
        <p><%= text_field_tag 'name' %></p>
    <% end %>
    #=> <fieldset><p><input id="name" name="name" type="text" /></p></fieldset>

#### サブフォームのタイトルを指定

    <%= field_set_tag 'Your details' do %>
        <p><%= text_field_tag 'name' %></p>
    <% end %>
    #=> <fieldset><legend>Your details</legend><p><input id="name" name="name" type="text" /></p></fieldset>


### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_tag_helper.rb#L650)

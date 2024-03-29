---
layout: page
---

### 説明

サブミットボタンを生成

### 使い方

    submit_tag(ボタンの名前='Save changes', オプション={}, HTML属性={} or イベント属性={})

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

#### サブミットボタンを生成

    submit_tag
    #=> <input name="commit" data-disable-with="Save changes" type="submit" value="Save changes" />

#### value値を設定

    submit_tag "Edit this article"
    #=> <input name="commit" data-disable-with="Edit this article" type="submit" value="Edit this article" />

#### 無効化

    submit_tag "Save edits", disabled: true
    #=> <input disabled="disabled" name="commit" data-disable-with="Save edits" type="submit" value="Save edits" />

#### data属性を設定

    submit_tag "Complete sale", data: { disable_with: "Submitting..." }
    #=> <input name="commit" data-disable-with="Submitting..." type="submit" value="Complete sale" />

#### value値が無い

    submit_tag nil, class: "form_submit"
    #=> <input class="form_submit" name="commit" type="submit" />

#### class属性を設定

    submit_tag "Edit", class: "edit_button"
    #=> <input class="edit_button" data-disable-with="Edit" name="commit" type="submit" value="Edit" />

#### 確認ダイアログ

    submit_tag "Save", data: { confirm: "Are you sure?" }
    #=> <input name='commit' type='submit' value='Save' data-disable-with="Save" data-confirm="Are you sure?" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_tag_helper.rb#L517)

---
layout: page
---

### 説明

パスワード入力ボックスを生成

### 使い方

    password_field(オブジェクト名, メソッド名, オプション={})

    # f.object
    f.password_field(メソッド名, オプション={})

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :size      | フォームの幅                         |
| :maxlength | 入力フィールドに入力可能な最大文字数 |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
| :disabled  | 無効化                               |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### 例

#### パスワード入力ボックスを生成

    password_field :page, :pass
    #=> <input id="page_pass" name="page[pass]" size="30" type="password" />

#### 初期値あり

    password_field :page, :pass
    #=> <input id="page_pass" name="page[pass]" size="30" type="password" value="abc" />

#### フォームの幅

    password_field :page, :pass, :size = '40'
    #=> <input id="page_pass" name="page[pass]" size="40" type="password" />

#### パスワード入力ボックスを生成(f.password_field)

    f.password_field :pass
    #=> <input id="page_pass" name="page[pass]" size="30" type="password" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1186)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1792)

---
layout: page
---

### 説明

電話番号入力ボックスを生成

### 使い方

    telephone_field(オブジェクト名, メソッド名, オプション={})
    phone_field(オブジェクト名, メソッド名, オプション={})

    # f.object
    f.telephone_field(メソッド名, オプション={})
    f.phone_field(メソッド名, オプション={})

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

#### 電話番号入力ボックスを生成

    telephone_field("user", "phone")
    #=> <input id="user_phone" name="user[phone]" type="tel" />

#### 電話番号入力ボックスを生成(f.telephone_field)

    f.telephone_field("phone")

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1397)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1844)

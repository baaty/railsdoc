---
layout: page
---

### 説明

週の入力欄を生成

### 使い方

    week_field(名前, メソッド名, オプション={})

    # f.object
    f.week_field(メソッド名, オプション={})

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :min       | 最少値                               |
| :max       | 最大値                               |
| :step      | 許容値の粒度                         |
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

#### 週の入力欄を生成(week_field)

    week_field("user", "born_on")
    #=> <input id="user_born_on" name="user[born_on]" type="week" />

#### 週の入力欄を生成(f.week_field)

    f.week_field("user", "born_on")
    #=> <input id="user_born_on" name="user[born_on]" type="week" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1530)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1935)

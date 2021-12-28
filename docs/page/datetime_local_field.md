---
layout: page
---

### 説明

ローカル日時の入力欄を生成  
datetime_fieldの別名

### 使い方

    datetime_local_field(要素名, メソッド名, オプション={})

    # f.object
    f.datetime_local_field(メソッド名, オプション={})

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

#### 日時の入力欄を生成

    datetime_local_field("user", "born_on")
    #=> <input id="user_born_on" name="user[born_on]" type="datetime-local" />

#### 日付指定

    @user.born_on = Date.new(1984, 1, 12)
    datetime_local_field("user", "born_on")
    #=> <input id="user_born_on" name="user[born_on]" type="datetime-local" value="1984-01-12T00:00:00" />

#### 時間指定

    datetime_local_field("user", "born_on", min: Date.today)
    #=> <input id="user_born_on" name="user[born_on]" type="datetime-local" min="2014-05-20T00:00:00.000" />

#### ISO8601形式の日時を指定

    datetime_local_field("user", "born_on", min: "2014-05-20T00:00:00")
    #=> <input id="user_born_on" name="user[born_on]" type="datetime-local" min="2014-05-20T00:00:00.000" />

#### 日時の入力欄を生成(f.datetime_local_field)

    f.datetime_local_field("born_on")
    #=> <input id="user_born_on" name="user[born_on]" type="datetime-local" />

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1498)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1909)

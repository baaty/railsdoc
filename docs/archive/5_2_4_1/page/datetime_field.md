---
layout: archive_page
---
### 説明
日時の入力欄を生成

### 使い方
    datetime_field(要素名 [, value値, オプション or HTML属性 or イベント属性])

### オプション

オプション        | 説明
-------------|--------------------
:min         | 最少値
:max         | 最大値
:step        | 許容値の粒度
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

### HTML属性

HTML属性      | 説明
-----------|-------------------
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### 日時の入力欄を生成
    datetime_field("user", "born_on")
    # <input id="user_born_on" name="user[born_on]" type="datetime-local" />

#### 日付指定
    @user.born_on = Date.new(1984, 1, 12)
    datetime_field("user", "born_on")
    # <input id="user_born_on" name="user[born_on]" type="datetime-local" value="1984-01-12T00:00:00" />

#### 時間指定
    datetime_field("user", "born_on", min: Date.today)
    # <input id="user_born_on" name="user[born_on]" type="datetime-local" min="2014-05-20T00:00:00.000" />

#### ISO8601形式の日時を指定
    datetime_field("user", "born_on", min: "2014-05-20T00:00:00")
    # <input id="user_born_on" name="user[born_on]" type="datetime-local" min="2014-05-20T00:00:00.000" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_helper.rb#L1446)

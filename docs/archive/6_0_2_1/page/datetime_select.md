---
layout: page
---
### 説明
日時の入力に特化した選択ボックスを生成

### 使い方
    datetime_select(オブジェクト名, メソッド名 [, オプション or HTML属性 or イベント属性])

#### f.object
    f.datetime_select(メソッド名 [, オプション or HTML属性 or イベント属性])

### オプション

オプション                  | 説明
-----------------------|-------------------
:use_month_numbers     | 月を数字で表示
:use_two_digit_numbers | 月と日を2桁表示
:use_short_month       | 月名を省略形で表示
:add_month_numbers     | 数値 + 月名表示
:use_month_names       | 月名をカスタマイズ
:date_separator        | 年月日の区切り文字
:start_year            | 開始年
:end_year              | 終了年
:minute_step           | 分の間隔を変更
:discard_day           | 日の選択ボックスを非表示
:discard_month         | 月の選択ボックスを非表示
:discard_year          | 年の選択ボックスを非表示
:order                 | 並び順を指定
:include_blank         | 空を含めて表示
:default               | デフォルトの日付を設定
:selected              | 優先した設定
:disabled              | 無効化
:prompt                | 選択値の一番上を指定
:with_css_classes      | スタイルを変更するタグの設定
:discard_type          | 名前の型を破棄
:prefix                | 名前の接頭辞を設定
:size                  | フォームの幅
:maxlength             | 入力フィールドに入力可能な最大文字数

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
#### datetime_select
##### 日時の入力に特化した選択ボックスを生成
    datetime_select :page, :updated_at
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月を数字で表示
    datetime_select :page, :updated_at, use_month_numbers: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月名を省略形で表示
    datetime_select :page, :updated_at, use_short_month: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 数値 + 月名表示
    datetime_select :page, :updated_at, add_month_numbers: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 年の範囲を2011から2013で１０分間隔
    datetime_select :page, :updated_at, start_year: 2012, end_year: 2013, minute_step: 10
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2010">2010</option>
    --- 省略 ---
    # </select>

#### f.datetime_select
##### 日時の入力に特化した選択ボックスを生成
    f.datetime_select :updated_at
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月を数字で表示
    f.datetime_select :updated_at, use_month_numbers: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月名を省略形で表示
    f.datetime_select :updated_at, use_short_month: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 数値 + 月名表示
    f.datetime_select :updated_at, add_month_numbers: true
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 年の範囲を2011から2013で１０分間隔
    f.datetime_select :updated_at, start_year: 2012, end_year: 2013, minute_step: 10
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2010">2010</option>
    # <option selected="selected" value="2011">2011</option>
    --- 省略 ---
    # </select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/date_helper.rb#L358)
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/date_helper.rb#L1195)
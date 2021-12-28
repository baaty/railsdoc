---
layout: page
---

### 説明

日にち選択ボックスを生成

### 使い方

    select_day(日付, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション             | 説明                         |
| ---------------------- | ---------------------------- |
| :use_month_numbers     | 月を数字で表示               |
| :use_two_digit_numbers | 月と日を2桁表示              |
| :use_short_month       | 月名を省略形で表示           |
| :add_month_numbers     | 数値 + 月名表示              |
| :use_month_names       | 月名をカスタマイズ           |
| :month_format_string   | フォーマット                 |
| :date_separator        | 年月日の区切り文字           |
| :time_separator        | 時間の区切り文字             |
| :datetime_separator    | 日付と時間の区切り文字       |
| :start_year            | 開始年                       |
| :end_year              | 終了年                       |
| :year_format           | 年選択の年の形式を設定       |
| :discard_day           | 日の選択ボックスを非表示     |
| :discard_month         | 月の選択ボックスを非表示     |
| :discard_year          | 年の選択ボックスを非表示     |
| :order                 | 並び順を指定                 |
| :include_blank         | 空を含めて表示               |
| :default               | デフォルトの日付を設定       |
| :selected              | 優先した設定                 |
| :disabled              | 無効化                       |
| :prompt                | 選択値の一番上を指定         |
| :with_css_classes      | スタイルを変更するタグの設定 |
| :use_hidden            | 非表示のタグのみ生成         |

### HTML属性

| HTML属性      | 説明                                 |
| ------------- | ------------------------------------ |
| :discard_type | 名前の型を破棄                       |
| :prefix       | 名前の接頭辞を設定                   |
| :size         | フォームの幅                         |
| :maxlength    | 入力フィールドに入力可能な最大文字数 |
| :accept       | フォームで受付可能なMIMEタイプ       |
| :readonly     | フォームの内容変更禁止               |
| :tabindex     | Tabキーによる入力欄の移動順          |
| :accesskey    | フォームに移動するショートカットキー |
| :id           | 要素固有の識別子                     |
| :class        | 要素を分類するクラス名               |
| :title        | 要素の補足情報                       |
| :style        | 要素の補足情報                       |
| :dir          | 表記方向                             |
| :lang         | 基本言語                             |

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
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### 指定された日にちをデフォルトとする日にち選択を生成

    my_date = Time.now + 2.days
    select_day(my_date)

#### 指定された数をデフォルトとする日にち選択を生成

    select_day(5)

#### 日にちを2桁で表示

    select_day(5, use_two_digit_numbers: true)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/date_helper.rb#L593)

---
layout: page
---
### date_select
#### 説明
日付の入力に特化した選択ボックスを生成

#### 使い方
    date_select(オブジェクト名 プロパティ名 [, オプション])

#### 使用できるフォームタグ
* form_tag

#### オプション

オプション                  | 説明
---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:use_month_numbers     | 月を数字で表示
:use_two_digit_numbers | 月と日を2桁表示
:use_short_month       | 月名を省略形で表示
:add_month_numbers     | 数値 + 月名表示
:use_month_names       | 月名をカスタマイズ
:month_format_string   |
:date_separator        | 年月日の区切り文字
:start_year            | 開始年
:end_year              | 終了年
:discard_day           | 日の選択ボックスを非表示
:discard_month         | 月の選択ボックスを非表示
:discard_year          | 年の選択ボックスを非表示
:order                 | 並び順を指定
:include_blank         | 空を含めて表示
:default               | デフォルトの日付を設定
:selected              | 優先した設定
:disabled              | 選択を無効
:prompt                | 選択値の一番上を指定
:with_css_classes      | スタイルを変更するタグの設定
:discard_type          | 名前の型を破棄
:prefix                | 名前の接頭辞を設定
:size                  | フォームの幅
:maxlength             | 入力フィールドに入力可能な最大文字数
:accept                | フォームで受付可能なMIMEタイプ
:readonly              | フォームの内容変更禁止
:disabled              | フォームの項目の利用禁止
:tabindex              | Tabキーによる入力欄の移動順
:accesskey             | フォームに移動するショートカットキー
:id                    | 要素固有の識別子
:class                 | 要素を分類するクラス名
:title                 | 要素の補足情報
:style                 | 要素の補足情報
:dir                   | 表記方向
:lang                  | 基本言語

#### 例
##### 基本形(オプションなし)
    <%= datetime_select_tag :page, :updated_at %>

    # 生成されるHTML
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月を数字で表示
    <%= datetime_select_tag :page, :updated_at, :use_month_numbers => true %>

    # 生成されるHTML
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 月名を省略形で表示
    <%= datetime_select_tag :page, :updated_at, :use_short_month => true %>

    # 生成されるHTML
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 数値 + 月名表示
    <%= datetime_select_tag :page, :updated_at, :add_month_numbers => true %>

    # 生成されるHTML
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2006">2006</option>
    --- 省略 ---
    # </select>

##### 年の範囲を2011から2013で１０分間隔
    <%= datetime_select_tag :page, :updated_at, :start_year => 2012, :end_year => 2013, :minute_step => 10  %>

    # 生成されるHTML
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <select id="page_updated_at_1i" name="page[updated_at(1i)]">
    # <option value="2010">2010</option>
    --- 省略 ---
    # </select>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/97f2c4129ae23ee074986a588628acc689a86462/actionview/lib/action_view/helpers/date_helper.rb#L257)

### f.date_select
#### 説明
日付の入力に特化した選択ボックスを生成

#### 使い方
    f.date_select(プロパティ名 [, オプション])

#### 使用できるフォームタグ
* form_for

#### オプション

オプション              | 説明
------------------ | ------------------
:use_month_numbers | 月を数字で表示
:use_short_month   | 月名を省略形で表示
:add_month_numbers | 数値 + 月名表示
:use_month_names   | 月名をカスタマイズ
:date_separator    | 年月日の区切り文字
:start_year        | 開始年
:end_year          | 終了年
:discard_day       | 日の選択ボックスを非表示
:discard_month     | 月の選択ボックスを非表示
:discard_year      | 年の選択ボックスを非表示
:order             | 並び順を指定
:include_blank     | 空を含めて表示
:include_seconds   | 秒数選択ボックスを表示
:default           | デフォルトの日付を設定
:disabled          | 選択を無効
:prompt            | 選択値の一番上を指定
:discard_type      | 名前の型を破棄
:prefix            | 名前の接頭辞を設定
:size              | フォームの幅
:maxlength         | 入力フィールドに入力可能な最大文字数
:accept            | フォームで受付可能なMIMEタイプ
:readonly          | フォームの内容変更禁止
:disabled          | フォームの項目の利用禁止
:tabindex          | Tabキーによる入力欄の移動順
:accesskey         | フォームに移動するショートカットキー
:id                | 要素固有の識別子
:class             | 要素を分類するクラス名
:title             | 要素の補足情報
:style             | 要素の補足情報
:dir               | 表記方向
:lang              | 基本言語

#### 例

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/97f2c4129ae23ee074986a588628acc689a86462/actionview/lib/action_view/helpers/date_helper.rb#L1069)
---
layout: archive_page
---
### 説明
時間の入力に特化した選択ボックスを生成

### 使い方
    time_select(オブジェクト名 メソッド名 [, オプション or HTML属性 or イベント属性])

#### f.object
    f.time_select(メソッド名 [, オプション])

### オプション

オプション            | 説明
-----------------|-------------
:include_seconds | 秒数選択ボックス
:ampm            | AM/PM形式
:ignore_date     | 未入力の場合に送信されない
:order           | 並び順を指定
:include_blank   | 空を含めて表示
:include_seconds | 秒数選択ボックスを表示
:default         | デフォルトの日付を設定
:disabled        | 無効化
:prompt          | 選択値の一番上を指定
:time_separator  | 時刻の区切り文字
:discard_type    | 名前の型を破棄
:prefix          | 名前の接頭辞を設定
:size            | フィールドの高さ
:multiple        | 複数選択可能

### HTML属性

HTML属性   | 説明
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
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### time_select
##### 時間の入力に特化した選択ボックスを生成
    time_select("article", "sunrise")

##### 秒数選択ボックスを表示
    time_select("article", "start_time", include_seconds: true)

##### 00, 15, 30, and 45を取得
    time_select 'game', 'game_time', {minute_step: 15}

##### AM/PM形式
    time_select 'game', 'game_time', {ampm: true}

#### f.time_select
##### 時間の入力に特化した選択ボックスを生成
    f.time_select :average_lap


* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/date_helper.rb#L319)
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/date_helper.rb#L1139)
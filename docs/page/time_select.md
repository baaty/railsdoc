---
layout: page
---
### time_select
#### 説明
時間の入力に特化した選択ボックスを生成

#### 使い方
    time_select(オブジェクト名 メソッド名 [, オプション])

#### オプション

オプション         | 説明
---------------- | ---------------
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
:tabindex        | Tabキーによる入力欄の移動順
:id              | 要素固有の識別子
:class           | 要素を分類するクラス名
:title           | 要素の補足情報
:style           | 要素の補足情報
:dir             | 表記方向
:lang            | 基本言語

#### 例
    # Creates a time select tag that, when POSTed, will be stored in the article variable in the sunrise attribute.
    time_select("article", "sunrise")

    # Creates a time select tag with a seconds field that, when POSTed, will be stored in the article variables in
    # the sunrise attribute.
    time_select("article", "start_time", include_seconds: true)

    # You can set the <tt>:minute_step</tt> to 15 which will give you: 00, 15, 30 and 45.
    time_select 'game', 'game_time', {minute_step: 15}

    # Creates a time select tag with a custom prompt. Use <tt>prompt: true</tt> for generic prompts.
    time_select("article", "written_on", prompt: {hour: 'Choose hour', minute: 'Choose minute', second: 'Choose seconds'})
    time_select("article", "written_on", prompt: {hour: true}) # generic prompt for hours
    time_select("article", "written_on", prompt: true) # generic prompts for all

    # You can set :ampm option to true which will show the hours as: 12 PM, 01 AM .. 11 PM.
    time_select 'game', 'game_time', {ampm: true}

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/date_helper.rb#L323)

### f.time_select
#### 説明
時間の入力に特化した選択ボックスを生成

#### 使い方
    f.time_select(メソッド名 [, オプション])

#### オプション

オプション            | 説明
---------------- | ---------------
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
:tabindex        | Tabキーによる入力欄の移動順
:id              | 要素固有の識別子
:class           | 要素を分類するクラス名
:title           | 要素の補足情報
:style           | 要素の補足情報
:dir             | 表記方向
:lang            | 基本言語

#### 例
    <%= form_for @race do |f| %>
      <%= f.time_select :average_lap %>
      <%= f.submit %>
    <% end %>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/date_helper.rb#L1183)
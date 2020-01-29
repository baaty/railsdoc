---
layout: page
---
### 説明
文字列から特定の部分のみ抽出

### 使い方
    excerpt(対象の文字列, 検索する文字列 [, オプション])

### オプション

オプション     | 説明          | デフォルト
--------- | ----------- | -----
:radius   | 抜き出す前後の文字数  | 100
:omission | 抽出時に付与する文字列 | ...

### 例
#### Railsの前後5文字を抽出
    <%= excerpt('RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', :radius => 5) %>
    # RubyとRails3の基本か...

#### 前後3文字を抽出して、･･･を付与
    <%= excerpt('RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', :radius => 3, :omission => "･･･") %>
    # ･･･byとRails3の基･･･

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0e50b7bdf4c0f789db37e22dc45c52b082f674b4/actionview/lib/action_view/helpers/text_helper.rb#L168)
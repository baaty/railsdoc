---
layout: page
---
### 説明
文字列を切り捨てる

### 使い方
    truncate(文字列 [, オプション])

### オプション

オプション   | 説明                        | デフォルト値
---------- | --------------------------- | -----
:length    | 切り捨ての桁数                | 30
:separator | 切り捨てる箇所を表す文字列      |
:omission  | 切り捨て時に末尾に付与する文字列 | ...

### 例
#### 30文字で切り捨てる
    truncate("RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説")
    # RubyとRails3の基本からビュー、モデル、コント...

#### 30文字以内の「、」で切り捨てる
    truncate("RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説", separator: "、")
    # RubyとRails3の基本からビュー、モデル、...

#### 30文字で切り捨て、末尾の文字列を追加
    truncate("RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説", omission: "・・・")
    # RubyとRails3の基本からビュー、モデル、コント・・・

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/text_helper.rb#L94)
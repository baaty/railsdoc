---
layout: page
---
### 説明
文字列から特定の部分のみ抽出

### 使い方
    excerpt(対象の文字列, 検索する文字列 [, オプション])

### オプション

オプション      | 説明                | デフォルト値
-----------|-------------------|-------
:radius    | 抜き出す前後の文字数   | 100
:omission  | 抽出時に付与する文字列 | ...
:separator | 区切り文字           |

### 例
#### Railsの前後5文字を抽出
    excerpt('RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', radius: 5)
    # RubyとRails3の基本か...

#### 前後3文字を抽出して、･･･を付与
    excerpt('RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', radius: 3, omission: "･･･")
    # ･･･byとRails3の基･･･

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/text_helper.rb#L175)
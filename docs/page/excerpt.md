---
layout: page
---

### 説明

文字列から特定の部分のみ抽出

### 使い方

    excerpt(対象の文字列, 検索する文字列, オプション={})

### オプション

| オプション | 説明                   | デフォルト値 |
| ---------- | ---------------------- | ------------ |
| :radius    | 抜き出す前後の文字数   | 100          |
| :omission  | 抽出時に付与する文字列 | ...          |
| :separator | 区切り文字             |              |

### 例

#### Railsの前後2文字を抽出

    excerpt('文字列から特定の部分のみを抽出する', '特定', radius: 2)
    #=> RubyとRails7の基本か...

#### 前後3文字を抽出して、･･･を付与

    excerpt('RubyとRails7の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', radius: 3, omission: "･･･")
    #=> ･･･byとRails7の基･･･

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L179)

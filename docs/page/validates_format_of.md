---
layout: page
---
### 説明
正規表現パターンに一致しているか検証

### 使い方
    validates_format_of(検証するフィールド名 [, ...])

### オプション

オプション        | 説明                      | 初期値
-------------|-------------------------|-----------------
:message     | 検証が失敗したときに表示するメッセージ | must be accepted
:with        | 正規表現パターン              |
:without     | 正規表現パターン              |
:multiline   | 行の先頭または、末尾           |
:on          | 検証を実行するタイミング         | 保存時
:allow_nil   | nilの検証をスキップ     | false
:allow_blank | nilや空文字の検証をスキップ      | false
:if          | 検証する条件を指定           |
:unless      | 検証しない条件を指定          |
:strict      | 検証に失敗した場合に例外を発生 |

### 例
#### 正規表現パターンに一致しているか検証
    validates_format_of :email, with: /\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\z/, on: :create

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/c551178f1b210c6becdf9612814e1c33fbcca2a5/activemodel/lib/active_model/validations/format.rb#L108)
---
layout: page
---
### 説明
値が空でないかを検証

### 使い方
    validates_presence_of(検証対象 [, ...])

### オプション

オプション        | 説明                      |
-------------|-------------------------|------
:message     | 検証が失敗したときに表示するメッセージ |
:on          | 検証を実行するタイミング         | 保存時
:allow_nil   | nilの検証をスキップ     | false
:allow_blank | nilや空文字の検証をスキップ      | false
:if          | 検証する条件を指定           |
:unless      | 検証しない条件を指定          |
:strict      | 検証に失敗した場合に例外を発生 |

### 例
#### 値が空でないかを検証
    validates_presence_of :first_name

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/presence.rb#L34)
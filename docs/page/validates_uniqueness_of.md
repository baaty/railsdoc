---
layout: page
---
### 説明
属性の値が一意であることを検証

### 使い方
    validates_uniqueness_of(検証するフィールド名 [, オプション])

### オプション

オプション           | 説明                           | デフォルト値
----------------|------------------------------|-------
:message        | 検証が失敗したときに表示するメッセージ      |
:scope          | 一意性制約を決めるために使用する他のカラム |
:conditions     | 検索条件を指定                  |
:case_sensitive | 大文字と小文字を区別するか          | true
:on             | 検証を実行するタイミング         | 保存時
:allow_nil      | nilの検証をスキップ          | false
:allow_blank    | nilや空文字の検証をスキップ           | false
:if             | 検証する条件を指定                |
:unless         | 検証しない条件を指定               |
:strict         | 検証に失敗した場合に例外を発生      |

### 例
#### 属性の値が一意であることを検証
    validates_uniqueness_of :user_name, scope: :account_id

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/98d33e3789adc098a1b866aee1d637660018270c/activerecord/lib/active_record/validations/uniqueness.rb#L224)
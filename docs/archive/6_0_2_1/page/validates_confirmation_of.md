---
layout: page
---
### 説明
2つのフィールドが等しいかバリデーション

### 使い方
    validates_confirmation_of(フィールド名 [, ...])

### オプション

オプション           | 説明                      | 初期値
----------------|-------------------------|-----------------
:message        | 失敗したときに表示するメッセージ | must be accepted
:case_sensitive | 完全一致                  | true
:on             | 実行するタイミング         | 保存時
:allow_nil      | nilをスキップ     | false
:allow_blank    | nilや空文字をスキップ      | false
:if             | バリデーションする条件を指定           |
:unless         | バリデーションしない条件を指定          |
:strict         | 失敗した場合に例外を発生 |

### 例
#### 2つのフィールドが等しいかバリデーション
      validates_confirmation_of :user_name, :password

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/exclusion.rb#L41)
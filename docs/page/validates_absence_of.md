---
layout: page
---
### 説明
指定した要素が空白であることを検証
保存時にデフォルトで実行される

### 使い方
    validates_absence_of(検証するフィールド名 [, ...])

### オプション

オプション        | 説明                      | 初期値
-------------|-------------------------|-----------------
:message     | 検証が失敗したときに表示するメッセージ | must be accepted
:on          | 保存されるタイミングを設定         |
:allow_nil   | trueならば、nilの検証はスキップ     | false
:allow_blank | trueならば、空の検証はスキップ      | false
:if          | 検証する条件を指定           |
:unless      | 検証しない条件を指定          |
:strict      | 検証に失敗した場合に例外を発生 |

### 例
#### 指定した要素が空白であることを検証
    class Person < ActiveRecord::Base
      validates_acceptance_of :terms_of_service
      validates_acceptance_of :eula, message: 'must be abided'
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/absence.rb#L26)
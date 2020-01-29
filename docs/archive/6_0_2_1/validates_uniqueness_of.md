---
layout: page
---
### 説明
属性の値が一意であることを検証

### 使い方
    validates_uniqueness_of(検証するフィールド名 [, オプション])

### オプション

オプション        | 説明                                | デフォルト値
--------------- | ----------------------------------- | -------
:message        | 検証が失敗したときに表示するメッセージ     |
:scope          | 一意性制約を決めるために使用する他のカラム |
:conditions     | 検索条件を指定                         |
:case_sensitive | 大文字と小文字を区別するか               | true
:allow_nil      | trueならば、nilの検証はスキップ          | false
:allow_blank    | trueならば、空の検証はスキップ           | false
:if             | 検証する条件を指定                      |
:unless         | 検証しない条件を指定                    |

### 例
    class User < ActiveRecord::Base
      validates_uniqueness_of :user_name, scope: :account_id
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/98d33e3789adc098a1b866aee1d637660018270c/activerecord/lib/active_record/validations/uniqueness.rb#L224)
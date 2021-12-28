---
layout: page
---
### 説明
文字列の長さをチェック

### 使い方
    validates_length_of(するフィールド名 [, ...])

### オプション

オプション         | 説明                        | デフォルト値
--------------|---------------------------|-------
:minimum      | 最小の文字列長               |
:maximum      | 最大の文字列長               |
:is           | 長さが同じこと                   |
:within       | 文字列長の範囲               |
:in           | 文字列長の範囲               |
:too_long     | :maximumに違反したときの、エラーメッセージ |
:too_short    | :minimumに違反したときの、エラーメッセージ |
:wrong_length | :isに違反したときの、エラーメッセージ      |
:message      | 失敗したときに表示するメッセージ   |
:tokenizer    | 文字列の分割方法             |
:on           | 実行するタイミング         | 保存時
:allow_nil    | nilをスキップ       | false
:allow_blank  | nilや空文字をスキップ        | false
:if           | バリデーションする条件を指定             |
:unless       | バリデーションしない条件を指定            |
:strict       | 失敗した場合に例外を発生   |

### 例
#### 文字列の長さをチェック
    class Person < ActiveRecord::Base
      validates_length_of :first_name, maximum: 30
      validates_length_of :last_name, maximum: 30, message: "less than 30 if you don't mind"
      validates_length_of :fax, in: 7..32, allow_nil: true
      validates_length_of :phone, in: 7..32, allow_blank: true
      validates_length_of :user_name, within: 6..20, too_long: 'pick a shorter name', too_short: 'pick a longer name'
      validates_length_of :zip_code, minimum: 5, too_short: 'please enter at least 5 characters'
      validates_length_of :smurf_leader, is: 4, message: "papa is spelled with 4 characters... don't play me."
      validates_length_of :essay, minimum: 100, too_short: 'Your essay must be at least 100 words.',
                          tokenizer: ->(str) { str.scan(/\w+/) }
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/fe49f432c9a88256de753a3f2263553677bd7136/activemodel/lib/active_model/validations/length.rb#L119)
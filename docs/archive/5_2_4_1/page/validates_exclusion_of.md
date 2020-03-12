---
layout: archive_page
---
### 説明
値が配列・範囲に含まれていないかバリデーション

### 使い方
    validates_exclusion_of(フィールド名 [, ...])

### オプション

オプション        | 説明                             | 初期値
-------------|--------------------------------|-----------------
:in          | 比較対象の配列、または範囲オブジェクト      |
:within      | 比較対象の配列、または範囲オブジェクトの範囲 |
:message     | 失敗したときに表示するメッセージ        | must be accepted
:on          | 実行するタイミング         | 保存時
:allow_nil   | nilをスキップ            | false
:allow_blank | nilや空文字をスキップ             | false
:if          | バリデーションする条件を指定                  |
:unless      | バリデーションしない条件を指定                 |
:strict      | 失敗した場合に例外を発生        |

### 例
#### 値が配列・範囲に含まれていないかバリデーション
    class Person < ActiveRecord::Base
      validates_exclusion_of :username, in: %w( admin superuser ), message: "You don't belong here"
      validates_exclusion_of :age, in: 30..60, message: 'This site is only for under 30 and over 60'
      validates_exclusion_of :format, in: %w( mov avi ), message: "extension %{value} is not allowed"
      validates_exclusion_of :password, in: ->(person) { [person.username, person.first_name] },
                             message: 'should not be the same as your username or first name'
      validates_exclusion_of :karma, in: :reserved_karmas
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/exclusion.rb#L44)
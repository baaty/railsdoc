---
layout: page
---
### 説明
値が配列・範囲に含まれていないか検証

### 使い方
    validates_exclusion_of(検証するフィールド名 [, ...])

### オプション

オプション        | 説明                             | 初期値
-------------|--------------------------------|-----------------
:in          | 比較対象の配列、または範囲オブジェクト      |
:within      | 比較対象の配列、または範囲オブジェクトの範囲 |
:message     | 検証が失敗したときに表示するメッセージ        | must be accepted
:on          | 保存されるタイミングを設定                |
:allow_nil   | trueならば、nilの検証はスキップ            | false
:allow_blank | trueならば、空の検証はスキップ             | false
:if          | 検証する条件を指定                  |
:unless      | 検証しない条件を指定                 |
:strict      | 検証に失敗した場合に例外を発生        |

### 例
#### 値が配列・範囲に含まれていないか検証
    class Person < ActiveRecord::Base
      validates_exclusion_of :username, in: %w( admin superuser ), message: "You don't belong here"
      validates_exclusion_of :age, in: 30..60, message: 'This site is only for under 30 and over 60'
      validates_exclusion_of :format, in: %w( mov avi ), message: "extension %{value} is not allowed"
      validates_exclusion_of :password, in: ->(person) { [person.username, person.first_name] },
                             message: 'should not be the same as your username or first name'
      validates_exclusion_of :karma, in: :reserved_karmas
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/exclusion.rb#L41)
---
layout: page
---
### 説明
値が配列・範囲に含まれているか検証

### 使い方
    validates_inclusion_of(検証するフィールド名 [, ...])

### オプション

オプション        | 説明                             | 初期値
-------------|--------------------------------|-----------------
:in          | 文字列長の範囲(range型)           |
:within      | 比較対象の配列、または範囲オブジェクトの範囲 |
:message     | 検証が失敗したときに表示するメッセージ        | must be accepted
:on          | 保存されるタイミングを設定                |
:allow_nil   | trueならば、nilの検証はスキップ            | false
:allow_blank | trueならば、空の検証はスキップ             | false
:if          | 検証する条件を指定                  |
:unless      | 検証しない条件を指定                 |
:strict      | 検証に失敗した場合に例外を発生        |

### 例
#### 値が配列・範囲に含まれているか検証
    class Person < ActiveRecord::Base
      validates_inclusion_of :gender, in: %w( m f )
      validates_inclusion_of :age, in: 0..99
      validates_inclusion_of :format, in: %w( jpg gif png ), message: "extension %{value} is not included in the list"
      validates_inclusion_of :states, in: ->(person) { STATES[person.country] }
      validates_inclusion_of :karma, in: :available_karmas
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/inclusion.rb#L41)
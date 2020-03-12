---
layout: archive_page
---
### 説明
値が配列・範囲に含まれているかバリデーション

### 使い方
    validates_inclusion_of(フィールド名 [, ...])

### オプション

オプション        | 説明                             | 初期値
-------------|--------------------------------|-----------------
:in          | 文字列長の範囲(range型)           |
:within      | 比較対象の配列、または範囲オブジェクトの範囲 |
:message     | 失敗したときに表示するメッセージ        | must be accepted
:on          | 実行するタイミング         | 保存時
:allow_nil   | nilをスキップ            | false
:allow_blank | nilや空文字をスキップ             | false
:if          | バリデーションする条件を指定                  |
:unless      | バリデーションしない条件を指定                 |
:strict      | 失敗した場合に例外を発生        |

### 例
#### 値が配列・範囲に含まれているかバリデーション
    class Person < ActiveRecord::Base
      validates_inclusion_of :gender, in: %w( m f )
      validates_inclusion_of :age, in: 0..99
      validates_inclusion_of :format, in: %w( jpg gif png ), message: "extension %{value} is not included in the list"
      validates_inclusion_of :states, in: ->(person) { STATES[person.country] }
      validates_inclusion_of :karma, in: :available_karmas
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/inclusion.rb#L42)
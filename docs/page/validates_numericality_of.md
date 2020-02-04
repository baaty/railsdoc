---
layout: page
---
### 説明
数値の大小、型を検証

### 使い方
    validates_numericality_of(検証するフィールド名 [, ...])

### オプション

オプション                     | 説明                      |
--------------------------|-------------------------|----
:message                  | 検証が失敗したときに表示するメッセージ |
:only_integer             | 整数であるかを検証             |
:greater_than             | 指定値より大きいか             |
:greater_than_or_equal_to | 指定値以上か               |
:equal_to                 | 指定値と等しいか              |
:less_than                | 指定値未満か               |
:less_than_or_equal_to    | 指定値以下か               |
:odd                      | 奇数か                     |
:even                     | 偶数か                     |
:on                       | 保存されるタイミングを設定         |
:allow_nil                | trueならば、nilの検証はスキップ     | false
:allow_blank              | trueならば、空の検証はスキップ      | false
:if                       | 検証する条件を指定           |
:unless                   | 検証しない条件を指定          |
:strict                   | 検証に失敗した場合に例外を発生 |

### 例
#### 数値の大小、型を検証
    validates_numericality_of :value, on: :create

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f888fad4db6d6956b675ca0441baa5aa63edae32/activemodel/lib/active_model/validations/numericality.rb#L154)
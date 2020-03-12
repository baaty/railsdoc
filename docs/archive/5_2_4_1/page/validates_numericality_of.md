---
layout: archive_page
---
### 説明
数値の大小、型をバリデーション

### 使い方
    validates_numericality_of(フィールド名 [, ...])

### オプション

オプション                     | 説明                      |
--------------------------|-------------------------|----
:message                  | 失敗したときに表示するメッセージ |
:only_integer             | 整数であるか             |
:greater_than             | 指定値より大きいか             |
:greater_than_or_equal_to | 指定値以上か               |
:equal_to                 | 指定値と等しいか              |
:less_than                | 指定値未満か               |
:less_than_or_equal_to    | 指定値以下か               |
:odd                      | 奇数か                     |
:even                     | 偶数か                     |
:on                       | 実行するタイミング         | 保存時
:allow_nil                | nilをスキップ     | false
:allow_blank              | nilや空文字をスキップ      | false
:if                       | バリデーションする条件を指定           |
:unless                   | バリデーションしない条件を指定          |
:strict                   | 失敗した場合に例外を発生 |

### 例
#### 数値の大小、型をバリデーション
    validates_numericality_of :value, on: :create

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/numericality.rb#L184)
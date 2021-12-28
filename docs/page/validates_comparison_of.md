---
layout: page
---

### 説明

指定された属性の値がすべて満たすかどうかを検証

### 使い方

    validates_comparison_of(属性名..)

### オプション

| オプション                | 説明                             |        |
| ------------------------- | -------------------------------- | ------ |
| :message                  | 失敗したときに表示するメッセージ |        |
| :greater_than             | 指定値より大きいか               |        |
| :greater_than_or_equal_to | 指定値以上か                     |        |
| :equal_to                 | 指定値と等しいか                 |        |
| :less_than                | 指定値未満か                     |        |
| :less_than_or_equal_to    | 指定値以下か                     |        |
| :on                       | 実行するタイミング               | 保存時 |
| :allow_nil                | nilをスキップ                    | false  |
| :allow_blank              | nilや空文字をスキップ            | false  |
| :if                       | バリデーションする条件を指定     |        |
| :unless                   | バリデーションしない条件を指定   |        |
| :strict                   | 失敗した場合に例外を発生         |        |
| :only_integer             | 整数であるか                     |        |

### 例

    class Person < ActiveRecord::Base
      validates_comparison_of :value, greater_than: 'the sum of its parts'
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/comparison.rb#L77)

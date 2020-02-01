---
layout: page
---
### 説明
数値を丸める

### 使い方
    number_with_precision(数値 [, オプション])

### オプション

オプション                      | 説明 | デフォルト値
-------------------------- | ---------------------------- | ----
:locale                    | 使用するロケール |
:precision                 | 小数以下の桁数 | 3
:signigicant               | 全体桁数 | false
:separator                 | 小数点記号 | .
:delimiter                 | 桁区切り文字 | ,
:strip_insignidicant_zeros | 小数点以下の0を削除 | false
:raise                     | 引数が無効な場合に、InvalidNumberError |

### 例
#### 数値を特定の桁で丸める
    number_with_delimiter(12345678)
    # 12,345,678

#### 数字
    number_with_delimiter("123456")
    # 123,456

#### 小数点
    number_with_delimiter(12345678.05)
    # 12,345,678.05

#### 区切り文字を変更
    number_with_delimiter(12345678, delimiter: ".")
    # 12.345.678

#### 少数点の区切り文字を変更
    number_with_delimiter(12345678.05, separator: " ")
    # 12,345,678 05

#### ロケール変更
    number_with_delimiter(12345678.05, locale: :fr)
    # 12 345 678,05

#### 文字が含まれる場合
    number_with_delimiter("112a")
    # 112a

#### 正規表現
    number_with_delimiter("123456.78", delimiter_pattern: /(\d+?)(?=(\d\d)+(\d)(?!\d))/)
    # 1,23,456.78

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/number_helper.rb#L249)
---
layout: page
---
### 説明
数値を特定の桁で丸める

### 使い方
    number_with_precision(数値 [, オプション])

### オプション

オプション                      | 説明
-------------------------- | ----------------------------
:locale                    | 使用するロケール
:precision                 | 小数以下の桁数
:signigicant               | 全体桁数
:separator                 | 小数点記号
:delimiter                 | 桁区切り文字
:strip_insignidicant_zeros | 小数点以下の0を削除
:raise                     | 引数が無効な場合に、InvalidNumberError

### 例
    number_with_delimiter(12345678)
    # 12,345,678

    number_with_delimiter("123456")
    # 123,456

    number_with_delimiter(12345678.05)
    # 12,345,678.05

    number_with_delimiter(12345678, delimiter: ".")
    # 12.345.678

    number_with_delimiter(12345678, delimiter: ",")
    # 12,345,678

    number_with_delimiter(12345678.05, separator: " ")
    # 12,345,678 05

    number_with_delimiter(12345678.05, locale: :fr)
    # 12 345 678,05

    number_with_delimiter("112a")
    # 112a

    number_with_delimiter(98765432.98, delimiter: " ", separator: ",")
    # 98 765 432,98

    number_with_delimiter("123456.78", delimiter_pattern: /(\d+?)(?=(\d\d)+(\d)(?!\d))/)
    # 1,23,456.78

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/number_helper.rb#L249)
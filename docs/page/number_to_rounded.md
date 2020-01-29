---
layout: page
---
### 説明
フォーマットの指定されたレベル

### 使い方
    number_to_rounded(数値 [, オプション])

### オプション

オプション                      | 説明                                            | デフォルト値
---------------------------|-----------------------------------------------|-------
:locale                    | 使用するロケール。YAML形式で「/config/locales/」以下の設定 |
:precision                 | 小数以下の桁数                                   | 2
:significant               | 精度                                            | false
:separator                 | 小数点記号                                      | .
:delimiter                 | 桁区切り文字                                     | ,
:strip_insignificant_zeros | 小数点以下の余分な0を削除                          | false

### 例
    number_to_rounded(111.2345)
    # 111.235

    number_to_rounded(111.2345, precision: 2)
    # 111.23

    number_to_rounded(13, precision: 5)
    # 13.00000

    number_to_rounded(389.32314, precision: 0)
    # 389

    number_to_rounded(111.2345, significant: true)
    # 111

    number_to_rounded(111.2345, precision: 1, significant: true)
    # 100

    number_to_rounded(13, precision: 5, significant: true)
    # 13.000

    number_to_rounded(111.234, locale: :fr)
    # 111,234

    number_to_rounded(13, precision: 5, significant: true, strip_insignificant_zeros: true)
    # 13

    number_to_rounded(389.32314, precision: 4, significant: true)
    # 389.3

    number_to_rounded(1111.2345, precision: 2, separator: ',', delimiter: '.')
    # 1.111,23

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/number_helper.rb#L226)
---
layout: archive_page
---
### 説明
数値を通貨のフォーマットに変換

### 使い方
    number_to_currency(数値 [, オプション])

### オプション

オプション                      | 説明                                            | デフォルト値
---------------------------|-------------------------------------------------|-------
:locale                    | 使用するロケール。YAML形式で「/config/locales/」以下の設定 |
:precision                 | 小数以下の桁数                                   | 2
:unit                      | 通貨単位                                        | $
:separator                 | 小数点記号                                      | .
:delimiter                 | 桁区切り文字                                     | ,
:format                    | 出力される文字のフォーマット                              | %u%n
:negative_format           | マイナスのときのフォーマット                                  | -%u%n

### 例
#### ドルの通過フォーマットに変換
    number_to_currency(123456789)
    # $123,456,789.00

#### 小数点5つまで表示
    number_to_currency(123456789, precision: 5)
    # $123,456,789.00000

#### 小数点をスペースで区切る
    number_to_currency(123456789, separator: " ")
    # $123,456,789 00

#### 桁区切りをスペース
    number_to_currency(123456789, delimiter: " ")
    # $123 456 789.00

#### 通過単位を「￥」
    number_to_currency(123456789, unit: "￥")
    # ￥123,456,789.00

#### 通過単位を後ろ
    number_to_currency(123456789, format: "%u%n", unit: "￥")
    # 123,456,789.00円

#### マイナスのフォーマット
    number_to_currency(-123456789, negative_format: "%u-%n")
    # $-123,456,789.00

#### 円のロケールを設定
    # config/locales/jp/yml
    jp:
      number:
        currency:
          format:
            unit: "円"
            format: "%n%u"
            negative_format: "-%n%u"
            precision: 0

    number_to_currency(123456789, locale: 'jp')
    # 123,456,789円

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/number_helper.rb#L103)
---
layout: archive_page
---
### 説明
数値を丸める

### 使い方
    number_to_rounded(数値 [, オプション])

### オプション

オプション                      | 説明                                            | デフォルト値
---------------------------|-----------------------------------------------|-------
:locale                    | 使用するロケール。YAML形式で「/config/locales/」以下の設定 |
:precision                 | 桁数                                            | 3
:significant               | 少数も桁数に含める                                  | false
:separator                 | 小数点記号                                      | .
:delimiter                 | 桁区切り文字                                     | ,
:strip_insignificant_zeros | 小数点以下の余分な0を削除                          | false

### 例
#### 数値を丸める
    number_to_rounded(111.2345)
    # 111.235

#### 小数点以下2桁で丸める
    number_to_rounded(111.2345, precision: 2)
    # 111.23

#### 少数以下5桁
    number_to_rounded(13, precision: 5)
    # 13.00000

#### 整数のみ
    number_to_rounded(389.32314, precision: 0)
    # 389

#### ３桁で丸める
    number_to_rounded(111.2345, significant: true)
    # 111

#### 1つめ桁で丸める
    number_to_rounded(111.2345, precision: 1, significant: true)
    # 100

#### ロケール指定
    number_to_rounded(111.234, locale: :fr)
    # 111,234

#### 区切り文字を変更
    number_to_rounded(1111.2345, precision: 2, separator: ',', delimiter: '.')
    # 1.111,23

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/number_helper.rb#L219)
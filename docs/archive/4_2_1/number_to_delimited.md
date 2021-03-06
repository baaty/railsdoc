---
layout: page
---
### 説明
数字を区切り文字を使用してグループ化

### 使い方
    number_to_delimited(数値 [, オプション])

### オプション

オプション      | 説明
---------- | --------------
:locale    | 使用するロケール
:delimiter | 桁区切り文字
:separator | 少数と整数の区切り文字を設定

### 例
    number_to_delimited(12345678)
    # 12,345,678

    number_to_delimited('123456')
    # 123,456

    number_to_delimited(12345678.05)
    # 12,345,678.05

    number_to_delimited(12345678, delimiter: '.')
    # 12.345.678

    number_to_delimited(12345678, delimiter: ',')
    # 12,345,678

    number_to_delimited(12345678.05, separator: ' ')
    # 12,345,678 05

    number_to_delimited(12345678.05, locale: :fr)
    # 12 345 678,05

    number_to_delimited('112a')
    # 112a

    number_to_delimited(98765432.98, delimiter: ' ', separator: ',')
    # => 98 765 432,98

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/44260581bec06e4ce05f3dd838c8b4736fc7eb1d/activesupport/lib/active_support/number_helper.rb#L150)
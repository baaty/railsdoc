---
layout: archive_page
---
### 説明
数字を区切り文字を使用してグループ化

### 使い方
    number_to_delimited(数値 [, オプション])

### オプション

オプション              | 説明
-------------------|---------------
:locale            | 使用するロケール
:delimiter         | 桁区切り文字
:separator         | 少数と整数の区切り文字を設定
:delimiter_pattern | 正規表現

### 例
#### 数字を区切り文字を使用してグループ化
    number_to_delimited(12345678)
    # 12,345,678

#### 数字を指定
    number_to_delimited('123456')
    # 123,456

#### 少数あり
    number_to_delimited(12345678.05)
    # 12,345,678.05

#### 区切り文字を変更
    number_to_delimited(12345678, delimiter: '.')
    # 12.345.678

#### 小数点の区切り文字を変更
    number_to_delimited(12345678.05, separator: ' ')
    # 12,345,678 05

#### ロケール変更
    number_to_delimited(12345678.05, locale: :fr)
    # 12 345 678,05

#### 文字が含まれる場合
    number_to_delimited('112a')
    # 112a

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/number_helper.rb#L175)
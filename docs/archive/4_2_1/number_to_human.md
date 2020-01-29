---
layout: page
---
### 説明
数値を単位のフォーマットに変換

### 使い方
    number_to_human(数値 [, オプション])

### オプション

オプション                      | 説明                                                                                                                                                        | デフォルト
-------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -----
:locale                    | 使用するロケール                                                                                                                                                  |
:precision                 | 桁数                                                                                                                                                        | 1
:signigicant               | 全体桁数                                                                                                                                                      |
:separator                 | 小数点記号                                                                                                                                                     | .
:delimiter                 | 桁区切り文字                                                                                                                                                    | ,
:strip_insignidicant_zeros | 小数点以下の0を削除                                                                                                                                                |
:units                     | 単位名を表すハッシュ

整数: :unit, :ten, :hundred, :thousand, :million, :billion, :trillion, :quadrillion

小数: :deci, :centi, :mili, :micro, :nano, :pico, :femto |
:format                    | 出力形式                                                                                                                                                      |

### 例
#### 単位で表示
    <%= number_to_human(123456789) %>
    # 123 Million

#### 5桁で表示
    <%= number_to_human(123456789, :precision => 5) %>
    # 123.00 Million

#### 小数点をスペースで区切る
    <%= number_to_human(123456789, :precision => 5, :separator => " ") %>
    # 123 00 Million

#### 単位を日本語仕様
    <%= number_to_human(123456789, :units => {:hundred => "百",:thousand => "千", :million => "百万", :billion => "十億", :trillion => "兆", :quadrillion => "千兆"}) %>
    # 123 百万

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/44260581bec06e4ce05f3dd838c8b4736fc7eb1d/actionview/lib/action_view/helpers/number_helper.rb#L376)
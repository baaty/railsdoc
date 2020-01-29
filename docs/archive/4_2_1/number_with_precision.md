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
    <%= number_with_precision(123456789) %>
    # 123456789.000

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/44260581bec06e4ce05f3dd838c8b4736fc7eb1d/actionview/lib/action_view/helpers/number_helper.rb#L224)
---
layout: page
---
### 説明
桁区切り文字を追加

### 使い方
    number_with_delimiter(数値 [, オプション])

### オプション

オプション      | 説明
---------- | ----------------------------
:locale    | 使用するロケール
:delimiter | 桁区切り文字
:separator | 小数点記号
:raise     | 引数が無効な場合に、InvalidNumberError

### 例
#### 桁区切り文字追加
    <%= number_with_delimiter(123456789) %>
    # 123,456,789

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/44260581bec06e4ce05f3dd838c8b4736fc7eb1d/actionview/lib/action_view/helpers/number_helper.rb#L179)
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
:delimiter_pattern | フォーマット
:raise     | 引数が無効な場合に、InvalidNumberError

### 例
#### 桁区切り文字追加
    <%= number_with_delimiter(123456789) %>
    # 123,456,789

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/number_helper.rb#L204)
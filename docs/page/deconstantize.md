---
layout: page
---
### 説明
文字列から右端のセグメントを削除

### 使い方
    文字列.deconstantize()

### 例
#### ::HTMPを削除
    'Net::HTTP'.deconstantize
    # "Net"

#### ::HTMPを削除
    '::Net::HTTP'.deconstantize
    # "::Net"

#### セグメントが1つ場合
    'String'.deconstantize
    # ""

#### 空文字の場合
    ''.deconstantize
    # ""

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L159)
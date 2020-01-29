---
layout: page
---
### 説明
文字列から右端のセグメントを削除する

### 使い方
    文字列.deconstantize()

### 例
    'Net::HTTP'.deconstantize
    # "Net"

    '::Net::HTTP'.deconstantize
    # "::Net"

    'String'.deconstantize
    # ""

    '::String'.deconstantize
    # ""

    ''.deconstantize
    # ""

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L159)
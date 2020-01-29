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
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/activesupport/lib/active_support/inflector/methods.rb#L216)
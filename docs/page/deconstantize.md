---
layout: page
---

### 説明

文字列から右端のセグメントを削除

### 使い方

    deconstantize(文字列)
    or
    文字列.deconstantize()

### 例

#### ::HTMPを削除

    deconstantize('Net::HTTP')
    # "Net"

#### ::HTMPを削除

    deconstantize('::Net::HTTP')
    # "::Net"

#### セグメントが1つ場合

    deconstantize('String')
    # ""

#### 空文字の場合

    deconstantize('')
    # ""

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/inflections.rb#L166)

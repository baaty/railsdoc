---
layout: archive_page
---
### 説明
文字列から右端のセグメントを削除

### 使い方
    deconstantize("文字列")
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L239)
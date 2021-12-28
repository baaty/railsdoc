---
layout: page
---

### 説明

定数式からモジュール部分を削除

### 使い方

    demodulize(文字列)
    or
    文字列.demodulize()

### 例

#### 定数式からモジュール部分を削除

    demodulize('ActiveRecord::CoreExtensions::String::Inflections')
    # "Inflections"

#### モジュール部分が無い

    demodulize('Inflections')
    # "Inflections"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/inflections.rb#L152)

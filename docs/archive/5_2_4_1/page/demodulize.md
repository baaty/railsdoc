---
layout: archive_page
---
### 説明
定数式からモジュール部分を削除

### 使い方
    demodulize("文字列")
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L221)
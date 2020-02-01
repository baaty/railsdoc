---
layout: page
---
### 説明
定数式からモジュール部分を削除

### 使い方
    文字列.demodulize()

### 例
#### 定数式からモジュール部分を削除
    'ActiveRecord::CoreExtensions::String::Inflections'.demodulize
    # "Inflections"

#### モジュール部分が無い
    'Inflections'.demodulize
    # "Inflections"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L146)
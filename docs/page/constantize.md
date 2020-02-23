---
layout: page
---
### 説明
指定した名前で定数を探す

### 使い方
    constantize("文字列")

### 例
    constantize('Module')
    # Module

    constantize('Test::Unit')
    # Test::Unit

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/inflector/methods.rb#L271)
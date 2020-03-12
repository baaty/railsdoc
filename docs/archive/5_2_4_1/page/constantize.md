---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L272)
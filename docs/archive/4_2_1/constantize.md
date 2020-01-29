---
layout: page
---
### 説明
引数の文字列で指定した名前で定数を探す

### 使い方
    文字列.constantize()

### 例
    'Module'.constantize     # => Module

    'Test::Unit'.constantize # => Test::Unit

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/activesupport/lib/active_support/inflector/methods.rb#L249)
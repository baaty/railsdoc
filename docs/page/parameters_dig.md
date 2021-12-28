---
layout: page
---

### 説明

与えられたキーからネストしたパラメータを参照

### 使い方

    dig(キー..)

### 例

    params = ActionController::Parameters.new(foo: { bar: { baz: 1 } })
    params.dig(:foo, :bar, :baz) #=> 1
    params.dig(:foo, :zot, :xyz) #=> nil
    params2 = ActionController::Parameters.new(foo: [10, 11, 12])
    params2.dig(:foo, 1) #=> 11

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L682)

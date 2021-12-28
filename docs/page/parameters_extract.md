---
layout: page
---

### 説明

与えられたキーにマッチするキーバリューを削除

### 使い方

    extract!(キー..)

### 例

    params = ActionController::Parameters.new(a: 1, b: 2, c: 3)
    params.extract!(:a, :b) #=> <ActionController::Parameters {"a"=>1, "b"=>2} permitted: false>
    params                  #=> <ActionController::Parameters {"c"=>3} permitted: false>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L720)

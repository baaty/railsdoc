---
layout: page
---

### 説明

与えられたキーだけを含む新しいActionController::Parametersインスタンスを作成

### 使い方

    slice(キー..)

### 例

    params = ActionController::Parameters.new(a: 1, b: 2, c: 3)
    params.slice(:a, :b) #=> <ActionController::Parameters {"a"=>1, "b"=>2} permitted: false>
    params.slice(:d)     #=> <ActionController::Parameters {} permitted: false>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L696)

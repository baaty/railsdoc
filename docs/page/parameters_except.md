---
layout: page
---

### 説明

与えられたキーをフィルタリングした新しいActionController::Parametersインスタンスを作成

### 使い方

    except(キー..)

### 例

    params = ActionController::Parameters.new(a: 1, b: 2, c: 3)
    params.except(:a, :b) #=> <ActionController::Parameters {"c"=>3} permitted: false>
    params.except(:d)     #=> <ActionController::Parameters {"a"=>1, "b"=>2, "c"=>3} permitted: false>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L711)

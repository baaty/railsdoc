---
layout: page
---

### 説明

指定されたキーのパラメータを参照

### 使い方

    fetch(キー, パラメータ..)

### 例

    params = ActionController::Parameters.new(person: { name: "Francesco" })
    params.fetch(:person)               #=> <ActionController::Parameters {"name"=>"Francesco"} permitted: false>
    params.fetch(:none)                 #=> ActionController::ParameterMissing: param is missing or the value is empty: none
    params.fetch(:none, {})             #=> <ActionController::Parameters {} permitted: false>
    params.fetch(:none, "Francesco")    #=> "Francesco"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L661)

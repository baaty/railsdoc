---
layout: page
---

### 説明

ActionController::Parametersの新しいインスタンスを作成

### 使い方

    new(パラメータ={}, ロギングコンテクスト={})

### 例

    class Person < ActiveRecord::Base
    end
    params = ActionController::Parameters.new(name: "Francesco")
    params.permitted?  #=> false
    Person.new(params) #=> ActiveModel::ForbiddenAttributesError
    ActionController::Parameters.permit_all_parameters = true
    params = ActionController::Parameters.new(name: "Francesco")
    params.permitted?  #=> true
    Person.new(params) #=> #<Person id: nil, name: "Francesco">

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L267)

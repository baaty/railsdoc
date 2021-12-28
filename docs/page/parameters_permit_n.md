---
layout: page
---

### 説明

permitted属性をtrueに設定

### 使い方

    permit!()

### 例

    class Person < ActiveRecord::Base
    end
    params = ActionController::Parameters.new(name: "Francesco")
    params.permitted?  #=> false
    Person.new(params) #=> ActiveModel::ForbiddenAttributesError
    params.permit!
    params.permitted?  #=> true
    Person.new(params) #=> #<Person id: nil, name: "Francesco">

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L428)

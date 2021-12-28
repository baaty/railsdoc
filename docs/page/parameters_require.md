---
layout: page
---

### 説明

指定したキーと関連する値が存在するか

### 使い方

    require(キー))

### 例

    ActionController::Parameters.new(person: { name: "Francesco" }).require(:person)
    #=> <ActionController::Parameters {"name"=>"Francesco"} permitted: false>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L489)

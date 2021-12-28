---
layout: page
---

### 説明

パラメータが許可されているか

### 使い方

    permitted?()

### 例

    params = ActionController::Parameters.new
    params.permitted? #=> false
    params.permit!
    params.permitted? #=> true

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L412)

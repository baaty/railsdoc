---
layout: page
---

### 説明

すべての許可されていないキーを削除したパラメータのActiveSupport::HashWithIndifferentAccess

### 使い方

    to_h()

### 例

    params = ActionController::Parameters.new({
    name: "Senjougahara Hitagi",
    oddity: "Heavy stone crab"
    })
    params.to_h
    #=> ActionController::UnfilteredParameters: unable to convert unpermitted parameters to hash
    safe_params = params.permit(:name)
    safe_params.to_h #=> {"name"=>"Senjougahara Hitagi"}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L300)

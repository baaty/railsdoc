---
layout: page
---

### 説明

URLクエリ文字列として使用するのに適した文字列

### 使い方

    to_query(引数..)

### 例

    params = ActionController::Parameters.new({
        name: "David",
        nationality: "Danish"
    })
    params.to_query
    #=> ActionController::UnfilteredParameters: unable to convert unpermitted parameters to hash
    safe_params = params.permit(:name, :nationality)
    safe_params.to_query
    #=> "name=David&nationality=Danish"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L352)

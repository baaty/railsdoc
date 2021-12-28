---
layout: page
---

### 説明

安全ではないフィルタリングされていないパラメータのActiveSupport::HashWithIndifferentAccessを参照

### 使い方

    to_unsafe_h()

### 例

    params = ActionController::Parameters.new({
    name: "Senjougahara Hitagi",
    oddity: "Heavy stone crab"
    })
    params.to_unsafe_h
    #=> {"name"=>"Senjougahara Hitagi", "oddity" => "Heavy stone crab"}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L367)

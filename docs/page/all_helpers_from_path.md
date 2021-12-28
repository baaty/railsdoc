---
layout: page
---

### 説明

指定されたパスに含まれるヘルパー名のリスト

### 使い方

    all_helpers_from_path(パス)

### 例

    ActionController::Base.all_helpers_from_path 'app/helpers'
    #=> ["application", "chart", "rubygems"]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/helpers.rb#L111)

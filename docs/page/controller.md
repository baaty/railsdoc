---
layout: page
---

### 説明

特定のコントローラにルートをスコープ

### 使い方

    controller(コントローラ)

### 例

    controller "food" do
        match "bacon", action: :bacon, via: :get
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L884)

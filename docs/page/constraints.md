---
layout: page
---

### 説明

ルールに基づいてネストされたルートを制約

### 使い方

    constraints(制約={}, ブロック引数)

### 例

    constraints(id: /\d+\.\d+/) do
        resources :posts
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L999)

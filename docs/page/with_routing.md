---
layout: page
---

### 説明

さまざまなルート構成を簡単にテストするためのヘルパー

### 使い方

    with_routing()

### 例

    with_routing do |set|
        set.draw do
            resources :users
        end
        assert_equal "/users", users_path
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L153)

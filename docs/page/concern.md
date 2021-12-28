---
layout: page
---

### 説明

ルーティング内などで使いまわせる共通のルーティングを定義

### 使い方

    concern(名前, コールバック=nil, ブロック引数)

### 例

#### 名前を使ってルーティングを定義

    concern :purchasable, Purchasable.new(returnable: true)

#### ブロック

    concern :commentable do |options|
      resources :comments, options
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L2048)

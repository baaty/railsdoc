---
layout: page
---
### 説明
ルーティング内などで使いまわせる共通のルーティングを定義

### 使い方
    concern(名前, [コールバック])

### 例
#### 名前を使ってルーティングを定義
    concern :purchasable, Purchasable.new(returnable: true)

#### ブロック
    concern :commentable do |options|
      resources :comments, options
    end


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L2043)
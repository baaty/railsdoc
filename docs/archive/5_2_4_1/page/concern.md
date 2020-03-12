---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/routing/mapper.rb#L2021)
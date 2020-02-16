---
layout: page
---
### 説明
カスタムURLヘルパーを定義  
ルーティングヘルパーのデフォルトの動作を置き換えることが可能  
directではnamespaceやスコープブロックないでは使用不可

### 使い方
    direct(名前 [, オプション]) do
      定義内容
    end

### 例
#### URL指定
    direct :homepage do
      "https://rubyonrails.org"
    end
    # hogepage_urlとhogepage_pathが使えるようになる

#### 配列を指定
    direct :commentable do |model|
      [ model, anchor: model.dom_id ]
    end

#### ハッシュを指定
    direct :main do
      { controller: "pages", action: "index", subdomain: "www" }
    end

#### デフォルト引数を指定
    direct :browse, page: 1, size: 10 do |options|
      [ :products, options.merge(params.permit(:page, :size).to_h.symbolize_keys) ]
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L2119)
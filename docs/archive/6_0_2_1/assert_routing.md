---
layout: page
---
### 説明
ルーティングとオプションの検証

### 使い方
    assert_routing(パス, オプション, nil, 追加パラメータ, メッセージ)

### 例
    assert_routing '/home', controller: 'home', action: 'index'

    assert_routing '/entries/show/23', controller: 'entries', action: 'show', id: 23

    assert_routing '/store', { controller: 'store', action: 'index' }, {}, {}, 'Route for store index not generated properly'

    assert_routing 'controller/action/9', {id: "9", item: "square"}, {controller: "controller", action: "action"}, {}, {item: "square"}

    assert_routing({ method: 'put', path: '/product/321' }, { controller: "product", action: "update", id: "321" })

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)
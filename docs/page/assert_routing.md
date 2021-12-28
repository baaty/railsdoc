---
layout: page
---

### 説明

ルーティングとオプションの確認

### 使い方

    assert_routing(パス, オプション, デフォルト={}, 追加パラメータ={}, メッセージ=nil)

### 例

#### ルーティングとオプションの確認

    assert_routing '/home', controller: 'home', action: 'index'

#### コントローラとアクションとパラメータで生成されたルーティング

    assert_routing '/entries/show/23', controller: 'entries', action: 'show', id: 23

#### エラーメッセージを確認

    assert_routing '/store', { controller: 'store', action: 'index' }, {}, {}, 'Route for store index not generated properly'

#### デフォルト値を確認

    assert_routing 'controller/action/9', {id: "9", item: "square"}, {controller: "controller", action: "action"}, {}, {item: "square"}

#### HTTPメソッドを指定

    assert_routing({ method: 'put', path: '/product/321' }, { controller: "product", action: "update", id: "321" })

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)

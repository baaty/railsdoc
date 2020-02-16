---
layout: page
---
### 説明
ルーティングとオプションのバリデーション

### 使い方
    assert_routing(パス, オプション, nil, 追加パラメータ, メッセージ)

### 例
#### ルーティングとオプションのバリデーション
    assert_routing '/home', controller: 'home', action: 'index'

#### コントローラとアクションとパラメータで生成されたルーティング
    assert_routing '/entries/show/23', controller: 'entries', action: 'show', id: 23

#### エラ〜メッセージをバリデーション
    assert_routing '/store', { controller: 'store', action: 'index' }, {}, {}, 'Route for store index not generated properly'

#### デフォルト値をバリデーション
    assert_routing 'controller/action/9', {id: "9", item: "square"}, {controller: "controller", action: "action"}, {}, {item: "square"}

#### HTTPメソッドを指定
    assert_routing({ method: 'put', path: '/product/321' }, { controller: "product", action: "update", id: "321" })

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)
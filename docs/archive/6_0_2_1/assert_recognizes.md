---
layout: page
---
### 説明
ルーティングやオプションの検証

### 使い方
    assert_recognizes(検証するオプション, パス, 追加パラメータ, メッセージ)

### 例
    assert_recognizes({controller: 'items', action: 'create'}, {path: 'items', method: :post})

    assert_recognizes({controller: 'items', action: 'list', id: '1', view: 'print'}, 'items/list/1', { view: "print" })

    assert_recognizes({controller: 'items', action: 'index'}, 'items')

    assert_recognizes({controller: 'items', action: 'list'}, 'items/list')

    assert_recognizes({controller: 'items', action: 'destroy', id: '1'}, 'items/destroy/1')

    assert_recognizes({controller: 'items', action: 'show', id: '1'}, 'view/item1')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)
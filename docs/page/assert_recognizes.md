---
layout: page
---

### 説明

指定したパスのルーティングやオプションの確認  
assert_generatesの逆の役割

### 使い方

    assert_recognizes(バリデーションするオプション, パス, 追加パラメータ={}, メッセージ=nil)

### 例

#### 指定したパスのルーティングやオプションのバリデーション

    assert_recognizes({controller: 'items', action: 'create'}, {path: 'items', method: :post})

#### パラメータもバリデーション

    assert_recognizes({controller: 'items', action: 'list', id: '1', view: 'print'}, 'items/list/1', { view: "print" })

#### デフォルトのルーティング

    assert_recognizes({controller: 'items', action: 'index'}, 'items')

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)

---
layout: page
---
### 説明
指定したパスのルーティングやオプションのバリデーション  
assert_generatesの逆の役割

### 使い方
    assert_recognizes(バリデーションするオプション, パス, 追加パラメータ, メッセージ)

### 例
#### 指定したパスのルーティングやオプションのバリデーション
    assert_recognizes({controller: 'items', action: 'create'}, {path: 'items', method: :post})

#### パラメータもバリデーション
    assert_recognizes({controller: 'items', action: 'list', id: '1', view: 'print'}, 'items/list/1', { view: "print" })

#### デフォルトのルーティング
    assert_recognizes({controller: 'items', action: 'index'}, 'items')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L47)
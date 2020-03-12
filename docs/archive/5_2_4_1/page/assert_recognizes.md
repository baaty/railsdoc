---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L42)
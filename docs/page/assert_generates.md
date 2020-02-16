---
layout: page
---
### 説明
指定したパスが生成できるかバリデーション  
assert_recognizesの逆の役割

### 使い方
    assert_generates(パス, オプション [, nil, 追加のパラメータ, メッセージ])

### 例
#### 指定したパスが生成できるかバリデーション
    assert_generates "/items", controller: "items", action: "index"

#### itemsコントローラにlistアクションがあるか
    assert_generates "/items/list", controller: "items", action: "list"

#### itemsコントローラのlistアクションにid=1があるか
    assert_generates "/items/list/1", { controller: "items", action: "list", id: "1" }

#### カスタムしたルーティング
    assert_generates "changesets/12", { controller: 'scm', action: 'show_diff', revision: "12" }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L85)
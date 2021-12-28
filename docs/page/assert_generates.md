---
layout: page
---

### 説明

指定したパスが生成できるか確認  
assert_recognizesの逆の役割

### 使い方

    assert_generates(パス, オプション, デフォルト={}, 追加のパラメータ={}, メッセージ=nil)

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

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/routing.rb#L85)

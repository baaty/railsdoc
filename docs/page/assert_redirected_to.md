---
layout: page
---

### 説明

リダイレクト先がどうなっているか確認

### 使い方

    assert_redirected_to(オプション={}, メッセージ=nil)

### 例

#### リダイレクト先がどうなっているかバリデーション

    assert_redirected_to controller: "weblog", action: "index"

#### 名前付きルーティング

    assert_redirected_to login_url

#### リダイレクト先が@customerのルーティングであるか

    assert_redirected_to @customer

#### 正規表現

    assert_redirected_to %r(\Ahttp://example.org)

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/response.rb#L53)

---
layout: archive_page
---
### 説明
リダイレクト先がどうなっているかバリデーション

### 使い方
    assert_redirected_to([オプション, メッセージ])

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/testing/assertions/response.rb#L55)
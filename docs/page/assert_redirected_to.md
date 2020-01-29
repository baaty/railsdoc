---
layout: page
---
### 説明
リダイレクト先がどうなっているか検証

### 使い方
    assert_redirected_to([オプション, メッセージ])

### 例
    assert_redirected_to controller: "weblog", action: "index"

    assert_redirected_to login_url

    assert_redirected_to @customer

    assert_redirected_to %r(\Ahttp://example.org)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/response.rb#L55)
---
layout: archive_page
---
### 説明
ステータスコードのバリデーション

### 使い方
    assert_response(タイプ [, メッセージ])

### タイプ名

メソッド    | 説明
--------- | -------
:success  | ステータスコードが200〜299
:redirect | ステータスコードが300〜399
:missing  | ステータスコードが404
:error    | ステータスコードが500〜599

### 例
#### ステータスコードのバリデーション
    assert_response :redirect

#### ステータスコードが401
    assert_response 401

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/testing/assertions/response.rb#L30)
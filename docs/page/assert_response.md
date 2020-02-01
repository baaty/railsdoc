---
layout: page
---
### 説明
ステータスコードの検証

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
#### ステータスコードの検証
    assert_response :redirect

#### ステータスコードが401
    assert_response 401

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/testing/assertions/response.rb#L30)
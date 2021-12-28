---
layout: page
---

### 説明

ステータスコードの確認

### 使い方

    assert_response(タイプ, メッセージ=nil)

### タイプ名

| メソッド  | 説明                       |
| --------- | -------------------------- |
| :success  | ステータスコードが200から299 |
| :redirect | ステータスコードが300から399 |
| :missing  | ステータスコードが404      |
| :error    | ステータスコードが500から599 |

### 例

#### ステータスコードのバリデーション

    assert_response :redirect

#### ステータスコードが401

    assert_response 401

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/assertions/response.rb#L30)

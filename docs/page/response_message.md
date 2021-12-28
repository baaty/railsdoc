---
layout: page
---

### 説明

HTTPステータスコードに対応するメッセージを取得

### 使い方

    response.message()

### 例

    response.status = 200
    response.message #=> "OK"
    response.status = 404
    response.message #=> "Not Found"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/http/response.rb#L298)

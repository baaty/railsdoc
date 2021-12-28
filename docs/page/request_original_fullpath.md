---
layout: page
---

### 説明

最後にリクエストされたパスをそのパラメターを含めて文字列で取得

### 使い方

    original_fullpath()

### 例

    # get '/foo'
    request.original_fullpath #=> '/foo'
    # get '/foo?bar'
    request.original_fullpath #=> '/foo?bar'

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/http/request.rb#L238)

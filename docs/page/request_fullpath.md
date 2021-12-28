---
layout: page
---

### 説明

最後にリクエストされたURLのパラメターを含むフルパス

### 使い方

    request.fullpath()

### 例

    # get "/articles"
    request.fullpath #=> "/articles"
    # get "/articles?page=2"
    request.fullpath #=> "/articles?page=2"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/http/request.rb#L249)

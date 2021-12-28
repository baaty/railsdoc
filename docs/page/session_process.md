---
layout: page
---

### 説明

実際のリクエストを実行

### 使い方

    process(HTTPメソッド, リクエストを実行するためのURI, params: パラメータ=nil, headers: 追加のヘッダー=nil, env: 追加のenv=nil, xhr: Ajaxリクエストを行いたいか=false, as: リクエストを異なるコンテントタイプでエンコード=nil)

### 例

    process :get, '/author', params: { since: 201501011400 }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/testing/integration.rb#L220)

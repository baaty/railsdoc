---
layout: page
---

### 説明

フラグメントキャッシュキーのプレフィックス

### 使い方

    fragment_cache_key(値=nil, キー引数)

### 例

    fragment_cache_key "v1"

### ブロック指定

    fragment_cache_key do
        @account.id.odd? ? "v1" : "v2"
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/abstract_controller/caching/fragments.rb#L57)

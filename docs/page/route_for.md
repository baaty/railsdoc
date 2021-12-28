---
layout: page
---

### 説明

ダイレクトまたは通常の名前のルート

### 使い方

    route_for(名前, パス..)

### 例

    resources :buckets
    direct :recordable do |recording|
        route_for(:bucket, recording.bucket)
    end
    direct :threadable do |threadable|
        route_for(:recordable, threadable.parent)
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/url_for.rb#L213)

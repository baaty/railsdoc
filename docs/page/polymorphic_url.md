---
layout: page
---

### 説明

指定されたレコードの名前付きRESTfulルートへの呼び出しを構築し結果のURL文字列を取得

### 使い方

    polymorphic_url(レコードのハッシュか配列, オプション={})

### オプション

| 名前          | 説明                                             |
| ------------- | ------------------------------------------------ |
| :action       | 指定されたルートのアクションプレフィックスを指定 |
| :routing_type | :path または :url                                |

### 例

    polymorphic_url(post) #=> "http://example.com/posts/1"
    polymorphic_url([blog, post]) #=> "http://example.com/blogs/1/posts/1"
    polymorphic_url([:admin, blog, post]) #=> "http://example.com/admin/blogs/1/posts/1"
    polymorphic_url([user, :blog, post]) #=> "http://example.com/users/1/blog/posts/1"
    polymorphic_url(Comment) #=> "http://example.com/comments"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/polymorphic_routes.rb#L101)

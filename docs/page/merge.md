---
layout: page
---

### 説明

他の条件とマージ

### 使い方

    モデル.merge(他の条件, *rest)


### 例

    Post.where(published: true).joins(:comments).merge( Comment.where(spam: false) )
    # Performs a single join query with both where conditions.

    recent_posts = Post.order('created_at DESC').first(5)
    Post.where(published: true).merge(recent_posts)
    # Returns the intersection of all published posts with the 5 most recently created posts.
    # (This is just an example. You'd probably want to do this with a single query!)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/spawn_methods.rb#L31)

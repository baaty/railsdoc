---
layout: page
---

### 説明

事前に設定したセレクト文を変更

### 使い方

    モデル.reselect(引数..)

### 例

    Post.select(:title, :body)
    # SELECT `posts`.`title`, `posts`.`body` FROM `posts`

    Post.select(:title, :body).reselect(:created_at)
    # SELECT `posts`.`created_at` FROM `posts`

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L316)

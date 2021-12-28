---
layout: page
---

### 説明

2つのリレーションをANDで繋ぐ

### 使い方

    モデルのリレーション.and(他のモデルのリレーション)

### 例

    Post.where(id: [1, 2]).and(Post.where(id: [2, 3]))
    # SELECT `posts`.* FROM `posts` WHERE `posts`.`id` IN (1, 2) AND `posts`.`id` IN (2, 3)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L810)

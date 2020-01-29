---
layout: page
---
### 説明
OR条件式

### 使い方
    モデル.or(条件式)

### 例
    Post.where("id = 1").or(Post.where("author_id = 3"))
    # SELECT `posts`.* FROM `posts` WHERE ((id = 1) OR (author_id = 3))

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L687)
---
layout: archive_page
---
### 説明
OR条件式

### 使い方
    モデル.or(条件式)

### 例
#### OR条件式
    Post.where("id = 1").or(Post.where("author_id = 3"))
    # SELECT `posts`.* FROM `posts` WHERE ((id = 1) OR (author_id = 3))

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L619)
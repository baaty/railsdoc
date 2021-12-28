---
layout: page
---

### 説明

与えられた関係がこの関係と構造的に互換性があるかどうかをチェックし、エラーを出さずにandやorのメソッドを使用できるかどうかを判断

### 使い方

    モデル.structurally_compatible?(調べる条件)


### 例

    Post.where("id = 1").structurally_compatible?(Post.where("author_id = 3"))
    #=> true

    Post.joins(:comments).structurally_compatible?(Post.where("id = 1"))
    #=> false

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L796)

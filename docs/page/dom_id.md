---
layout: page
---

### 説明

DOMのid規約に沿った名前を取得

### 使い方

    dom_id(レコード, prefix=nil)

### 例

    dom_id(Post.find(45))
    #=> "post_45"

    dom_id(Post.new)
    #=> "new_post"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/record_identifier.rb#L89)

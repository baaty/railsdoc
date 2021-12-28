---
layout: page
---

### 説明

すでに設定されているスコープを除いたモデルのスコープを取得

### 使い方

    unscoped(ブロック引数)

### 例

#### でに設定されているスコープを除いたモデルのスコープを取得

    Post.unscoped.all

#### ブロック

    Post.unscoped {
      Post.limit(10) # Fires "SELECT * FROM posts LIMIT 10"
    }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/scoping/default.rb#L42)

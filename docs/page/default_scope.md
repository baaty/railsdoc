---
layout: page
---

### 説明

デフォルトのスコープを定義

### 使い方

    default_scope(条件式=nil, all_queries: 全てのクエリ=nil, ブロック引数)

### 例

    class Article < ActiveRecord::Base
      default_scope { where(published: true) }
    end
    Article.all
    # SELECT * FROM articles WHERE published = true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/scoping/default.rb#L123)

---
layout: page
---
### 説明
レコードが参照されるテーブルを指定

### 使い方
    モデル.from(値 [, サブクエリ])

### 例
    Topic.select('title').from('posts')
    #=> SELECT title FROM posts

    Topic.select('title').from(Topic.approved)
    # => SELECT title FROM (SELECT * FROM topics WHERE approved = 't') subquery

    Topic.select('a.title').from(Topic.approved, :a)
    # => SELECT a.title FROM (SELECT * FROM topics WHERE approved = 't') a

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L754)
---
layout: page
---
### 説明
レコードが参照されるテーブルを指定

### 使い方
    モデル.from(値 [, サブクエリ])

### 例
    Topic.select('title').from('posts')
    # SELECT title FROM posts

    Topic.select('title').from(Topic.approved)
    # SELECT title FROM (SELECT * FROM topics WHERE approved = 't') subquery

    Topic.select('a.title').from(Topic.approved, :a)
    # SELECT a.title FROM (SELECT * FROM topics WHERE approved = 't') a

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L864)
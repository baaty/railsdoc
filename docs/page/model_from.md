---
layout: page
---

### 説明

レコードが参照されるテーブルを指定

### 使い方

    モデル.from(値, サブクエリ=nil)

### 例

#### レコードが参照されるテーブルを指定

    Topic.select('title').from('posts')
    # SELECT title FROM posts

#### 関連付けモデル

    Topic.select('title').from(Topic.approved)
    # SELECT title FROM (SELECT * FROM topics WHERE approved = 't') subquery

#### サブクエリ

    Topic.select('a.title').from(Topic.approved, :a)
    # SELECT a.title FROM (SELECT * FROM topics WHERE approved = 't') a

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1048)

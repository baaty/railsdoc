---
layout: archive_page
---
### 説明
レコードが参照されるテーブルを指定

### 使い方
    モデル.from(値 [, サブクエリ])

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L796)
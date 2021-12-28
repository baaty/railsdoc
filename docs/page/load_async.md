---
layout: page
---

### 説明

バックグラウンドのスレッドプールからクエリを実行するようにスケジュール

### 使い方

    モデル.load_async()

### 例

    Post.where(published: true).load_async
    #=> #<ActiveRecord::Relation>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L649)

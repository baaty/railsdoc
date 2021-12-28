---
layout: page
---

### 説明

レコードがまだ読み込まれていない場合にデータベースからレコードを読み込む

### 使い方

    モデル.load([ブロック])

### 例

    Post.where(published: true).load
    #=> #<ActiveRecord::Relation>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L678)

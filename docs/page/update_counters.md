---
layout: page
---

### 説明

現在のリレーションのレコードのカウンタを更新

### 使い方

    モデル.update_counters(ID, 条件)

### 例

    Post.where(author_id: author.id).update_counters(comment_count: 1)

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L516)

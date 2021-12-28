---
layout: page
---

### 説明

既存のwhere条件を上書き  
上書きされるのは指定したキーのみで、指定されていないwhereの条件はそのまま

### 使い方

    モデル.rewhere(条件)

### 例

#### 既存のwhere条件を上書き

    Post.where(trashed: true).rewhere(trashed: false)
    # WHERE `trashed` = 0

#### 指定したキーのみ上書き

    Post.where(active: true).where(trashed: true).rewhere(trashed: false)
    # WHERE `active` = 1 AND `trashed` = 0

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L738)

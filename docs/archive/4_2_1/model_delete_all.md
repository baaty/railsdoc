---
layout: page
---
### 使い方
    モデル.delete_all([検索条件])

### 例
    Post.delete_all("person_id = 5 AND (category = 'Something' OR category = 'Else')")

    Post.delete_all(["person_id = ? AND (category = ? OR category = ?)", 5, 'Something', 'Else'])

    Post.where(person_id: 5).where(category: ['Something', 'Else']).delete_all

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L442)
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L471)
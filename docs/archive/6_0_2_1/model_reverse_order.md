---
layout: page
---
### 説明
取得した値を特定のキーで逆順に並び替える

### 使い方
    モデル.reverse_order

### 例
#### pagesテーブルをcategory_idを逆順で並び替える
    Page.order("category_id").reverse_order

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L973)
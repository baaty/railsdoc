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
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L845)
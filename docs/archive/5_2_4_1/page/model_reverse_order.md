---
layout: archive_page
---
### 説明
取得した値を特定のキーで逆順に並び替える

### 使い方
    モデル.reverse_order()

### 例
#### pagesテーブルをcategory_idを逆順で並び替える
    Page.order("category_id").reverse_order

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L882)
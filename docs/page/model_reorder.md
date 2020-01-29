---
layout: page
---
### 説明
取得した値を特定のキーで逆順に並び替える

### 使い方
    モデル.reorder(ソート式)

### 例
#### 逆順で並び替える
    Page.order("category_id DESC")
    # SELECT "pages".* FROM "pages" ORDER BY category_id DESC

#### 2つのカラムを指定して並び替える
    User.order('name DESC, email')
    # SELECT "users".* FROM "users" ORDER BY name DESC, email

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L379)
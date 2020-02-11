---
layout: page
---
### 説明
指定した条件以外の条件をクエリから削除

### 使い方
    モデル.only(条件)

### 例
#### 条件式を削除
    Post.order('id asc').only(:where)

#### 複数指定
    Post.order('id asc').only(:where, :order)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/spawn_methods.rb#L65)
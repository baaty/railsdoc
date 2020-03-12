---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/spawn_methods.rb#L65)
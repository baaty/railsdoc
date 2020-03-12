---
layout: archive_page
---
### 説明
条件式を削除

### 使い方
    モデル.unscope(条件式)

### 例
#### 条件式を削除
    User.order('email DESC').unscope(:order) == User.all

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L363)
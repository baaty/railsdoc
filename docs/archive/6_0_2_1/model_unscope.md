---
layout: page
---
### 説明
条件式を削除

### 使い方
    モデル.unscope(条件式)

### 例
    User.order('email DESC').unscope(:order) == User.all

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L430)
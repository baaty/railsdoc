---
layout: page
---
### 説明
重複のない値を取得

### 使い方
    モデル.distinct([重複を削除するか])

### 例
    User.select(:name).distinct

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L883)
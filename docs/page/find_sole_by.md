---
layout: page
---

### 説明

条件を指定してレコードが1個しかない場合だけ取得

### 使い方

    モデル.find_sole_by(条件..)

### 例

    Product.find_sole_by(["price = %?", price])

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L129)

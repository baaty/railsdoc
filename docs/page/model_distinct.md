---
layout: page
---

### 説明

重複のない値を取得

### 使い方

    モデル.distinct(重複を削除するか=true)

### 例

#### 重複のない値を取得

    User.select(:name).distinct

#### 重複も削除

    User.select(:name).distinct(false)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1067)

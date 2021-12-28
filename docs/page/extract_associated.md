---
layout: page
---

### 説明

リレーションから名前付きのアソシエーションを抽出

### 使い方

    extract_associated(アソシエーション)

### 例

    account.memberships.extract_associated(:user)
    #=> Returns collection of User records

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L224)

---
layout: page
---

### 説明

アソシエーションが読み込まれたか

### 使い方

    モデル.loaded?()

### 例

    person.pets.loaded? #=> false
    person.pets.records
    person.pets.loaded? #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L51)

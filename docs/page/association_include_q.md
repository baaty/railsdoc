---
layout: page
---

### 説明

モデルのコレクションに指定したレコードが存在するか

### 使い方

    モデルのコレクション.include?(レコード)

### 例

    person.pets.include?(Pet.find(20))
    #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L925)

---
layout: page
---

### 説明

モデルのコレクションを生成して保存

### 使い方

    モデルのコレクション.delete(レコード..)

### 例

#### 生成して保存

    person.pets.delete(Pet.find(1))

#### 複数指定

    person.pets.delete(Pet.find(1), Pet.find(3))

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L618)

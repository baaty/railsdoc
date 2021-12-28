---
layout: page
---

### 説明

レコードをユニークにするか

### 使い方

    モデルのコレクション.distinct(ユニークにするか=true)

### 例

#### ユニークにする

    person.pets.select(:name).distinct

#### ユニークにしない

    person.pets.select(:name).distinct.distinct(false)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L695)

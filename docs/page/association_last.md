---
layout: page
---

### 説明

モデルのコレクションから最後のレコードを取得

### 使い方

    モデルのコレクション.last(取得する件数=nil)

### 例

#### 最後のレコードを取得

    person.pets.last
    #=> <Pet id: 3, name: "Choo-Choo", person_id: 1>

#### 複数件取得

    person.pets.last(2)
    #=> [
    #      <Pet id: 2, name: "Spook", person_id: 1>,
    #      <Pet id: 3, name: "Choo-Choo", person_id: 1>
    #    ]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L257)

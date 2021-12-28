---
layout: page
---

### 説明

モデルのコレクションから先頭のレコードを取得

### 使い方

    モデルのコレクション.first(取得する件数=nil)

### 例

#### 先頭のレコードを取得

    person.pets.first
    #=> <Pet id: 1, name: "Fancy-Fancy", person_id: 1>


#### 複数件取得

    person.pets.first(2)
    #=> [
    #      <Pet id: 1, name: "Fancy-Fancy", person_id: 1>,
    #      <Pet id: 2, name: "Spook", person_id: 1>
    #    ]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L142)

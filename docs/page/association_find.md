---
layout: page
---

### 説明

モデルのコレクションからIDを指定してレコードを取得

### 使い方

    モデルのコレクション.find(ID..)

### 例

#### IDを指定してレコードを取得

    person.pets.find(1)
    #=> <Pet id: 1, name: "Fancy-Fancy", person_id: 1>

#### 複数指定

    person.pets.find(2, 3)
    #=> [
    #       <Pet id: 2, name: "Spook", person_id: 1>,
    #       <Pet id: 3, name: "Choo-Choo", person_id: 1>
    #    ]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L136)

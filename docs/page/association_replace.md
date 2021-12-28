---
layout: page
---

### 説明

モデルのコレクションを他の配列で置き換える

### 使い方

    モデルのコレクション.replace(他の配列)

### 例

    person.pets
    #=> [<Pet id: 1, name: "Gorby", group: "cats", person_id: 1>]

    other_pets = [Pet.new(name: 'Puff', group: 'celebrities')]

    person.pets.replace(other_pets)

    person.pets
    #=> [<Pet id: 2, name: "Puff", group: "celebrities", person_id: 1>]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L389)

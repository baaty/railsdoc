---
layout: page
---

### 説明

空かチェック

### 使い方

    モデルのコレクション.any?()

### 例

#### 空かチェック

    class Person < ActiveRecord::Base
      has_many :pets
    end
    person.pets.count # 0
    person.pets.any?  # false
    person.pets << Pet.new(name: 'Snoop')
    person.pets.count # 0
    person.pets.any?  # true

#### ブロック

    person.pets
    # [<Pet name: "Snoop", group: "dogs">]

    person.pets.any? do |pet|
      pet.group == 'cats'
    end
    # false

    person.pets.any? do |pet|
      pet.group == 'dogs'
    end
    # true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L834)

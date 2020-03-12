---
layout: archive_page
---
### 説明
モデルが空かチェック

### 使い方
    モデル.any?([ブロック])

### 例
#### 基本的な使い方
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
    # [#<Pet name: "Snoop", group: "dogs">]

    person.pets.any? do |pet|
      pet.group == 'cats'
    end
    # false

    person.pets.any? do |pet|
      pet.group == 'dogs'
    end
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L871)
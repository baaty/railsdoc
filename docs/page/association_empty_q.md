---
layout: page
---

### 説明

空か

### 使い方

    モデルのコレクション.empty?()

### 例

    class Person < ActiveRecord::Base
        has_many :pets
    end

    person.pets.count  #=> 1
    person.pets.empty? #=> false

    person.pets.delete_all

    person.pets.count  #=> 0
    person.pets.empty? #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L829)

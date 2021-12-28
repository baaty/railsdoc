---
layout: page
---

### 説明

モデルのコレクションに複数のレコードがあるか  
2以上のレコードがある場合にtrue

### 使い方

    モデルのコレクション.many?()

### 例

    class Person < ActiveRecord::Base
        has_many :pets
    end

    person.pets.count #=> 1
    person.pets.many? #=> false

    person.pets << Pet.new(name: 'Snoopy')
    person.pets.count #=> 2
    person.pets.many? #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L875)

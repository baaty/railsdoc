---
layout: page
---

### 説明

モデルのコレクションの長さ

### 使い方

    モデルのコレクション.length()

### 例

    class Person < ActiveRecord::Base
        has_many :pets
    end

    person.pets.length #=> 3
    # executes something like SELECT "pets".* FROM "pets" WHERE "pets"."person_id" = 1

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L785)

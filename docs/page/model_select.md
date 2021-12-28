---
layout: page
---

### 説明

カラムを指定して取得

### 使い方

    モデル.select(カラム名..)

### 例

#### カラムを指定して取得

    person.pets.select(:id, :name)

#### ブロックで指定

    person.pets.select do |pet|
      pet.name =~ /oo/
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L288)

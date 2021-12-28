---
layout: page
---

### 説明

オブジェクトのシリアル化されたハッシュ

### 使い方

    serializable_hash(オプション=nil)

### 例

#### 色々な使用方法

    class Person
        include ActiveModel::Serialization
        attr_accessor :name, :age
        def attributes
            {'name' => nil, 'age' => nil}
        end
        def capitalized_name
            name.capitalize
        end
    end
    person = Person.new
    person.name = 'bob'
    person.age  = 22
    person.serializable_hash                #=> {"name"=>"bob", "age"=>22}
    person.serializable_hash(only: :name)   #=> {"name"=>"bob"}
    person.serializable_hash(except: :name) #=> {"age"=>22}
    person.serializable_hash(methods: :capitalized_name)
    #=> {"name"=>"bob", "age"=>22, "capitalized_name"=>"Bob"}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/serialization.rb#L125)

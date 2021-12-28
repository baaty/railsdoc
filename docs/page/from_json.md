---
layout: page
---

### 説明

JSON文字列からモデルの属性を設定

### 使い方

    モデル.from_json(JSON文字列, include_root=include_root_in_json)

### 例

    json = { name: 'bob', age: 22, awesome:true }.to_json
    person = Person.new
    person.from_json(json) #=> #<Person:0x007fec5e7a0088 @age=22, @awesome=true, @name="bob">
    person.name            #=> "bob"
    person.age             #=> 22
    person.awesome         #=> true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/serializers/json.rb#L146)

---
layout: page
---
### 使い方
    モデル.build([属性])

### 例
#### 引数なし
    person.pets.build
    # => #<Pet id: nil, name: nil, person_id: 1>

#### 属性
    person.pets.build(name: 'Fancy-Fancy')
    # => #<Pet id: nil, name: "Fancy-Fancy", person_id: 1>

#### ブロック
    person.pets.build([{name: 'Spook'}, {name: 'Choo-Choo'}, {name: 'Brain'}])
    # => [
    #      #<Pet id: nil, name: "Spook", person_id: 1>,
    #      #<Pet id: nil, name: "Choo-Choo", person_id: 1>,
    #      #<Pet id: nil, name: "Brain", person_id: 1>
    #    ]

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L258)
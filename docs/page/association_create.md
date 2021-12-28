---
layout: page
---

### 説明

モデルのコレクションを生成して保存

### 使い方

    モデルのコレクション.create(属性={}, ブロック引数)

### 例

#### 生成して保存

    person.pets.create(name: 'Fancy-Fancy')
    #=> <Pet id: 1, name: "Fancy-Fancy", person_id: 1>

#### 複数作成

    person.pets.create([{name: 'Spook'}, {name: 'Choo-Choo'}])
    #=> [
    #      <Pet id: 2, name: "Spook", person_id: 1>,
    #      <Pet id: 3, name: "Choo-Choo", person_id: 1>
    #    ]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L347)

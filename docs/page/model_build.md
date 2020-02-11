---
layout: page
---
### 説明
モデルオブジェクトを生成

newの別名

### 使い方
    モデル.build([属性])

### 例
#### モデルを生成
    person.pets.build
    # <Pet id: nil, name: nil, person_id: 1>

#### 属性を指定
    person.pets.build(name: 'Fancy-Fancy')
    # <Pet id: nil, name: "Fancy-Fancy", person_id: 1>

#### ブロックを指定
    person.pets.build([{name: 'Spook'}, {name: 'Choo-Choo'}, {name: 'Brain'}])
    # [
    #   <Pet id: nil, name: "Spook", person_id: 1>,
    #   <Pet id: nil, name: "Choo-Choo", person_id: 1>,
    #   <Pet id: nil, name: "Brain", person_id: 1>
    # ]

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L315)
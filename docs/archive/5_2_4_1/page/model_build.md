---
layout: archive_page
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

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L318)
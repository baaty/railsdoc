---
layout: archive_page
---
### 説明
カラムを指定して取得

### 使い方
    モデル.select(カラム名)

### 例
#### カラムを指定して取得
    person.pets.select(:id, :name)
    # [
    #   <Pet id: 1, name: "Fancy-Fancy">,
    #   <Pet id: 2, name: "Spook">,
    #   <Pet id: 3, name: "Choo-Choo">
    # ]

#### ブロックで指定
    person.pets.select { |pet| pet.name =~ /oo/ }
    # [
    #   <Pet id: 2, name: "Spook", person_id: 1>,
    #   <Pet id: 3, name: "Choo-Choo", person_id: 1>
    # ]


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/associations/collection_proxy.rb#L112)
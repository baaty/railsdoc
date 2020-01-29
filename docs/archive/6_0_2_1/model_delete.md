---
layout: page
---
### 説明
モデルを削除

### 使い方
    モデル.delete([引数 or 配列])

### 例
    person.pets.delete(Pet.find(1))
    # [<Pet id: 1, name: "Fancy-Fancy", person_id: 1>]

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L617)
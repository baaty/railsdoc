---
layout: page
---
### 説明
主キーを設定して、複数のレコードを追加

### 使い方
    モデル.concat(モデル)

### 例
    person.pets.concat(Pet.new(name: 'Fancy-Fancy'))

    person.pets.concat(Pet.new(name: 'Spook'), Pet.new(name: 'Choo-Choo')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/associations/collection_proxy.rb#L1025)
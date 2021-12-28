---
layout: page
---

### 説明

指定されたレコードを破棄しコレクションから削除  
dependentオプションを無視してデータベースからレコードが削除される

### 使い方

    モデルのコレクション.destroy(レコード..)

### 例

#### コレクションから削除 

    person.pets.destroy(Pet.find(1))

#### 複数指定

    person.pets.destroy(Pet.find(2), Pet.find(3))

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L690)

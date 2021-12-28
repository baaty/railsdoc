---
layout: page
---

### 説明

モデルのコレクションからカラムを指定して取得

### 使い方

    モデルのコレクション.select(カラム.., ブロック引数)

### 例

#### カラムを指定して取得

    person.pets.select(:name)

#### 複数カラム指定

    person.pets.select(:id, :name)

#### ブロック指定

    person.pets.select { |pet| /oo/.match?(pet.name) }

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L57)

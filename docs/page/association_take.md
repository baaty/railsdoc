---
layout: page
---

### 説明

モデルのコレクションの指定した数のレコードを取得

### 使い方

    モデルのコレクション.take(取得する件数=nil)

### 例

#### モデルのコレクションの指定した数のレコードを取得

    person.pets.take

#### 複数件取得

    person.pets.take(2)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L287)

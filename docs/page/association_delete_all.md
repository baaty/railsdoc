---
layout: page
---

### 説明

モデルのコレクションからすべてのレコードを削除  
dependentオプションが指定されている場合はそれに従う

### 使い方

    モデルのコレクション.delete_all(依存=nil)

### 例

    person.pets.delete_all

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L472)

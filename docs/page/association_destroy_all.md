---
layout: page
---

### 説明

データベースから直接コレクションのレコードを削除  
dependentオプションを無視してデータベースからレコードが削除される

### 使い方

    モデルのコレクション.destroy_all()

### 例

    person.pets.destroy_all

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L499)

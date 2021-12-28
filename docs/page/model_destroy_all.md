---
layout: page
---

### 説明

指定した条件のレコードと関連しているレコードをすべて削除  
dependentが設定されている場合は関連付けられたモデルも削除

### 使い方

    モデル.destroy_all()

### 例

    Person.where(age: 0..18).destroy_all


### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L499)

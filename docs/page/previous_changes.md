---
layout: page
---

### 説明

保存される前に変更された値をハッシュで取得

### 使い方

    モデル.previous_changes()

### 例

    person.name # "bob"
    person.name = 'robert'
    person.save
    person.previous_changes # {name: ["bob", "robert"]}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/dirty.rb#L241)

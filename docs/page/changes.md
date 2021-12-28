---
layout: page
---

### 説明

モデルの変更前と変更後の値をハッシュで取得

### 使い方

    モデル.changes()

### 例

    person.changes # {}
    person.name = 'bob'
    person.changes # {name: ["bill", "bob"]}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/dirty.rb#L232)

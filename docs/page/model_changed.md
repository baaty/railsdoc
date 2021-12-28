---
layout: page
---

### 説明

変更点を取得

### 使い方

    モデル.changed()

### 例

    person.changed # []
    person.name = 'bob'
    person.changed # ["name"]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/dirty.rb#L173)

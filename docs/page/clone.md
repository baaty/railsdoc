---
layout: page
---

### 説明

モデルのコピーを生成

### 使い方

    モデル.clone()

### 例

    user = User.first
    new_user = user.clone
    user.name               # "Bob"
    new_user.name = "Joe"
    user.name               # "Joe"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/core.rb#L513)

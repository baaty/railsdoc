---
layout: page
---

### 説明

シンボルまたはメソッドのエラーの配列

### 使い方

    モデル.errors[属性]

### 例

    person.errors[:name]
    #=> ["cannot be nil"]
    person.errors['name']
    #=> ["cannot be nil"]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb)

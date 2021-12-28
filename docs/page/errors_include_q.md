---
layout: page
---

### 説明

指定した属性が含まれているか

### 使い方

    モデル.errors.include?(属性)

### 例

    person.errors.messages
    #=> {:name=>["cannot be nil"]}
    person.errors.include?(:name)
    #=> true
    person.errors.include?(:age)
    #=> false

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L170)

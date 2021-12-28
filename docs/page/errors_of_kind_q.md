---
layout: page
---

### 説明

指定されたタイプの属性でエラーが発生したか

### 使い方

    モデル.errors.of_kind?(属性, タイプ=:invalid)

### 例

    person.errors.add :age
    person.errors.add :name, :too_long, { count: 25 }
    person.errors.of_kind? :age
    #=> true
    person.errors.of_kind? :name
    #=> false
    person.errors.of_kind? :name, :too_long
    #=> true
    person.errors.of_kind? :name, "is too long (maximum is 25 characters)"
    #=> true
    person.errors.of_kind? :name, :not_too_long
    #=> false
    person.errors.of_kind? :name, "is too long"
    #=> false

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L363)

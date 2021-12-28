---
layout: page
---

### 説明

モデルが指定したメソッドを呼び出せるかチェック

### 使い方

    モデル.respond_to?(メソッド名, include_private=false)

### 例

#### Personモデルがname属性を呼び出せるかチェック

    person.respond_to?(:name)
    # true

#### プライベートメソッドを呼び出せるかチェック

    person.respond_to?(:private_name, true)
    # true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods.rb#L207)

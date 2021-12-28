---
layout: page
---

### 説明

与えられたキー以外のすべてのエラーを削除

### 使い方

    モデル.errors.slice!(キー..)

### 例

    person.errors.keys
    #=> [:name, :age, :gender, :city]
    person.errors.slice!(:age, :gender)
    #=> { :name=>["cannot be nil"], :city=>["cannot be nil"] }
    person.errors.keys
    #=> [:age, :gender]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/83217025a171593547d1268651b446d3533e2019/activemodel/lib/active_model/errors.rb#L146)

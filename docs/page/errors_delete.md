---
layout: page
---

### 説明

指定した属性のエラーを削除

### 使い方

    モデル.errors.delete(属性, タイプ=nil, オプション引数)

### 例

    person.errors[:name]
    #=> ["cannot be nil"]
    person.errors.delete(:name)
    #=> ["cannot be nil"]
    person.errors[:name]
    #=> []

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L183)

---
layout: page
---

### 説明

属性のHashとそのエラーメッセージを取得

### 使い方

    モデル.errors.to_hash(完全なメッセージか=false)

### 例

    person.errors.to_hash
    #=> {:name=>["cannot be nil"]}
    person.errors.to_hash(true)
    #=> {:name=>["name cannot be nil"]}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L224)

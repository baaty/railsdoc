---
layout: page
---

### 説明

全てのエラーメッセージのキーを取得

### 使い方

    モデル.errors.keys()

### 例

    person.errors.messages
    #=> {:name=>["cannot be nil", "must be specified"]}
    person.errors.keys
    #=> [:name]

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/errors.rb#L214)

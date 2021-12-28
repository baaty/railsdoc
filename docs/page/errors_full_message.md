---
layout: page
---

### 説明

指定された属性の完全なエラーメッセージを取得

### 使い方

    モデル.errors.full_message(属性, メッセージ)

### 例

    person.errors.full_message(:name, 'is invalid')
    #=> "Name is invalid"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L419)

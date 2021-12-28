---
layout: page
---

### 説明

エラーのJSON

### 使い方

    モデル.errors.as_json(オプション=nil)

### 例

#### エラーのJSON

    person.errors.as_json
    #=> {:name=>["cannot be nil"]}

#### full_messages

    person.errors.as_json(full_messages: true)
    #=> {:name=>["name cannot be nil"]}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L215)

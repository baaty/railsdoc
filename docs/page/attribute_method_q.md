---
layout: page
---

### 説明

指定したモデルの属性が存在するかチェック

### 使い方

    モデル.attribute_method?(属性)

### 例

#### true

    User.attribute_method?(:name)
    # true

#### false

    User.attribute_method?(:age)
    # false

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods.rb#L150)

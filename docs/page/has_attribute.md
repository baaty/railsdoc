---
layout: page
---

### 説明

モデルに指定した属性が存在するかチェック

### 使い方

    モデル.has_attribute?(属性)

### 例

#### 指定した属性が存在する場合

    person.has_attribute?(:name)
    # true

#### 指定した属性が存在しない場合

    person.has_attribute?(:nothing)
    # false

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods.rb#L180)

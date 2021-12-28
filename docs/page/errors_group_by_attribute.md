---
layout: page
---

### 説明

属性のHashとErrorオブジェクトの配列を取得

### 使い方

    モデル.errors.group_by_attribute()

### 例

    person.errors.group_by_attribute
    #=> {:name=>[<#ActiveModel::Error>, <#ActiveModel::Error>]}

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L257)

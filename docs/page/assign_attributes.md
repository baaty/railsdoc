---
layout: page
---

### 説明

属性のハッシュを渡すことですべての属性を設定

### 使い方

    assign_attributes(属性のハッシュ)

### 例

    class Cat
      include ActiveModel::AttributeAssignment
      attr_accessor :name, :status
    end
    cat = Cat.new
    cat.assign_attributes(name: "Gorby", status: "yawning")
    cat.name #=> 'Gorby'
    cat.status #=> 'yawning'
    cat.assign_attributes(status: "sleeping")
    cat.name #=> 'Gorby'
    cat.status #=> 'sleeping'

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/attribute_assignment.rb#L28)

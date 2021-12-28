---
layout: page
---

### 説明

保存されていない変更が加えられた属性の元の値を示すハッシュ

### 使い方

    モデル.changed_attributes()

### 例

    person.name #=> "bob"
    person.name = 'robert'
    person.changed_attributes #=> {"name" => "bob"}

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/dirty.rb#L221)

---
layout: page
---

### 説明

指定された属性とタイプに一致するエラーが発生したか

### 使い方

    モデル.errors.added?(属性, タイプ=:invalid, オプション={})

### 例

    person.errors.add :name, :blank
    person.errors.added? :name, :blank
    # true

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L340)

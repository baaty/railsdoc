---
layout: page
---

### 説明

各エラーオブジェクトをイテレート

### 使い方

    モデル.errors.each(ブロック引数)

### 例

    person.errors.add(:name, :too_short, count: 2)
    person.errors.each do |error|
        # Will yield <#ActiveModel::Error attribute=name, type=too_short, options={:count=>3}>
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L67)

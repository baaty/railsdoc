---
layout: page
---

### 説明

新しいエラーを追加

### 使い方

    モデル.errors.add(属性, タイプ=:invalid, オプション引数)

### 例

#### 新しいエラーを追加

    person.errors.add(:name)
    # Adds <#ActiveModel::Error attribute=name, type=invalid>

#### typeを指定

    person.errors.add(:name, :not_implemented, message: "must be implemented")
    # Adds <#ActiveModel::Error attribute=name, type=not_implemented,
                            options={:message=>"must be implemented"}>

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L310)

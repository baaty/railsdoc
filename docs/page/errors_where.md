---
layout: page
---

### 説明

属性、タイプ、オプションに一致するエラーを検索

### 使い方

    モデル.errors.where(属性, タイプ=nil, オプション引数)

### 例

    person.errors.where(:name)
    #=> all name errors.
    person.errors.where(:name, :too_short)
    #=> all name errors being too short
    person.errors.where(:name, :too_short, minimum: 2)
    #=> all name errors being too short and minimum is 2

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/errors.rb#L157)

---
layout: page
---

### 説明

テーブル名からモデル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって可能

### 使い方

    classify(テーブル名)

### 例

    classify("people")
    # "Person"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/inflections.rb#L243)

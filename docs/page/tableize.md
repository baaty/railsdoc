---
layout: page
---

### 説明

モデル名からテーブル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方

    tableize(文字列)

### 例

#### モデル名からテーブル名へ変換  

    tableize("Page")
    # "pages"

#### アッパーキャメルケース

    tableize("AdminUser")
    # "admin_users"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/string/inflections.rb#L231)

---
layout: page
---
### 説明
モデル名からテーブル名へ変換
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方
    モデル.tableize

### 例
#### 「Page」を変換
    "Page".tableize
    # "pages"

#### 「AdminUser」を変換
    "AdminUser".tableize
    # "admin_users"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L205)
---
layout: archive_page
---
### 説明
モデル名からテーブル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方
    tableize(文字列)

### 例
#### 「Page」を変換
    tableize("Page")
    # "pages"

#### 「AdminUser」を変換
    tableize("AdminUser")
    # "admin_users"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L187)
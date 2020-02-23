---
layout: page
---
### 説明
クラス名からファイル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方
    underscore("文字列")

### 例

#### 「Product」を変換
    underscore("Product")
    # "product"

#### 「AdminUser」を変換
    underscore("AdminUser")
    # "admin_user"

#### 「Backoffice::Session」を変換
    underscore("Backoffice::Session")
    # "backoffice/session"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/inflector/methods.rb#L91)

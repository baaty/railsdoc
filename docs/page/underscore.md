---
layout: page
---

### 説明

クラス名からファイル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって追加

### 使い方

    underscore(文字列)

### 例

#### クラス名からファイル名へ変換 

    underscore("Product")
    # "product"

#### アッパーキャメルケース

    underscore("AdminUser")
    # "admin_user"

#### メソッド呼び出し

    underscore("Backoffice::Session")
    # "backoffice/session"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/inflector/methods.rb#L96)

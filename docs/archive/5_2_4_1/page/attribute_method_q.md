---
layout: archive_page
---
### 説明
指定したモデルの属性が存在するかチェック

### 使い方
    モデル.attribute_method?(属性)

### 例
#### true
    User.attribute_method?(:name)
    # true

#### false
    User.attribute_method?(:age)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L150)
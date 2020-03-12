---
layout: archive_page
---
### 説明
モデルに指定した属性が存在するかチェック

### 使い方
    モデル.has_attribute?(属性)

### 例
#### 指定した属性が存在する場合
    person.has_attribute?(:name)
    # true

#### 指定した属性が存在しない場合
    person.has_attribute?(:nothing)
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/attribute_methods.rb#L302)
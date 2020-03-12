---
layout: archive_page
---
### 説明
モデルが指定したメソッドを呼び出せるかチェック

### 使い方
    モデル.respond_to?(メソッド名 [, include_private=false])

### 例
#### Personモデルがname属性を呼び出せるかチェック
    person.respond_to?(:name)
    # true

#### プライベートメソッドを呼び出せるかチェック
    person.respond_to?(:private_name, true)
    # true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/attribute_methods.rb#L446)
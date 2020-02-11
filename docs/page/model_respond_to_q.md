---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/mime_responds.rb#L201)
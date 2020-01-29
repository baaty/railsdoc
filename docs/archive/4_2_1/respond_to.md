---
layout: page
---
### 説明
モデルに対して呼び出せるかチェック

### 使い方
    モデル.respond_to(名前 [, include_private=false])

### 例
    person.respond_to(:name)
    # => true

    person.respond_to(:name=)
    # => true

    person.respond_to(:name?)
    # => true

    person.respond_to('age')
    # => true

    person.respond_to('age=')
    # => true

    person.respond_to('age?')
    # => true

    person.respond_to(:nothing)
    # => false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L235)
---
layout: page
---
### 説明
例外が発生するかチェック

### 使い方
    モデル.instance_method_already_implemented?(属性)

### 例
    class Person < ActiveRecord::Base
      def save
        'already defined by Active Record'
      end
    end

    Person.instance_method_already_implemented?(:save)
    # => ActiveRecord::DangerousAttributeError: save is defined by ActiveRecord

    Person.instance_method_already_implemented?(:name)
    # => false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/08576b94ad4f19dfc368619d7751e211d23dcad8/activerecord/lib/active_record/attribute_methods.rb#L113)
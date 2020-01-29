---
layout: page
---
### 説明
URLのidの部分にid以外のものを指定

### 使い方
    class User < ActiveRecord::Base
      def to_param  # overridden
        name
      end
    end

### 例
    class User < ActiveRecord::Base
      def to_param  # overridden
        name
      end
    end

    user = User.find_by name: 'Phusion'
    user_path(user)  # => "/users/Phusion"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/bb075e3839d9eea2be5cb0cbed50dafa2c14bb37/activemodel/lib/active_model/conversion.rb#L71)
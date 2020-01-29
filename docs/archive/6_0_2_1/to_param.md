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
    user_path(user)
    # "/users/Phusion"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/integration.rb#L57)
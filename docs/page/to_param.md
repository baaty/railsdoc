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
#### URLのidの部分にid以外のものを指定
    class User < ActiveRecord::Base
      def to_param  # overridden
        name
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/integration.rb#L57)
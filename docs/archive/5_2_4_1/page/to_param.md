---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/conversion.rb#L82)
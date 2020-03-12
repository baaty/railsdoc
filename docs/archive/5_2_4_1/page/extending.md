---
layout: archive_page
---
### 説明
モジュールやブロックメソッドを引数に与えて、モデルをscopeで拡張  
返されたオブジェクトをさらに拡張することもできる

### 使い方
    モデル.extending(モジュール)

### 例
#### モジュール
    module Pagination
      def page(number)
        # pagination code goes here
      end
    end

    scope = Model.all.extending(Pagination)
    scope.page(params[:page])

#### ブロック
    module Pagination
      def page(number)
        # pagination code goes here
      end
    end

    scope = Model.all.extending do
      def page(number)
        # pagination code goes here
      end
    end
    scope.page(params[:page])

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/query_methods.rb#L861)
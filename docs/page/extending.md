---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L929)
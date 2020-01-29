---
layout: page
---
### 説明
モジュールやブロックメソッドを引数に与えて、モデルをscopeで拡張
返されたオブジェクトをさらに拡張することもできる

### 使い方
    モデル.extending(モジュール)

    モデル.extending(ブロック)

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
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L824)
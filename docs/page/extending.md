---
layout: page
---

### 説明

モジュールやブロックメソッドを引数に与えてモデルをscopeで拡張  
返されたオブジェクトをさらに拡張することもできる

### 使い方

    モデル.extending(モジュール.., ブロック引数)

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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1113)

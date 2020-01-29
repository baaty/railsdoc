---
layout: page
---
### 説明
アクションの前後に処理を実行

### 使い方
    around_action 名前

### 例
    around_action :t, only: :show
    def t
    end


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/callbacks.rb#L175)
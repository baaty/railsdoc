---
layout: page
---
### 説明
アクションの後に処理を実行

### 使い方
    after_action 名前

### 例
    after_action :render_form, only: [:new :edit]
    def render_form
      render 'form'
    end


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/callbacks.rb#L147)
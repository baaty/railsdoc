---
layout: page
---
### 説明
バリデーションの直前に呼び出されるメソッドを設定

### 使い方
    before_validation(引数 [, ...])

### 例
#### バリデーションの直前に呼び出されるメソッドを設定
    before_validation :remove_whitespaces
    private
    def remove_whitespaces
      name.strip!
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/callbacks.rb#L56)
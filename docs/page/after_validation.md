---
layout: page
---
### 説明
検証の直後に呼び出されるメソッド

### 使い方
    after_validation(メソッド名 [, ...])

### 例
    after_validation :set_status
    private
    def set_status
      self.status = errors.empty?
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/callbacks.rb#L97)
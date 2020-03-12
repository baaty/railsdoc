---
layout: archive_page
---
### 説明
バリデーションの直後に呼び出されるメソッド

### 使い方
    after_validation(メソッド名 [, ...])

### 例
    after_validation :set_status
    private
    def set_status
      self.status = errors.empty?
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/callbacks.rb#L97)
---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/callbacks.rb#L56)
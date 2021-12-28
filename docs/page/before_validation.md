---
layout: page
---

### 説明

バリデーションの直前に呼び出されるメソッドを設定

### 使い方

    before_validation(引数 [, ...])

### 例

    before_validation :remove_whitespaces
    private
    def remove_whitespaces
      name.strip!
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/callbacks.rb#L56)

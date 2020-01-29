---
layout: page
---
### 説明
チェックボックスのチェックが入っているか

### 使い方
    validates(検証するフィールド名, :numericality => 検証パラメータ)

### オプション

オプション                     | 説明
------------------------- | ---------
:only_integer             | 整数であるかを検証
:greater_than             | 指定値より大きいか
:greater_than_or_equal_to | 指定値以上か
:equal_to                 | 指定値と等しいか
:less_than                | 指定値未満か
:less_than_or_equal_to    | 指定値以下か
:odd                      | 奇数か
:even                     | 偶数か

### 例
    validates :age, numericality: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/validates.rb#L105)
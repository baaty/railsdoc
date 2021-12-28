---
layout: page
---
### 説明
デフォルトのコールバックを上書き

### 使い方
    define_model_callbacks(メソッド名 [, only: タイプ])

### タイプ

タイプ | 説明
---- | ----
:after | 後
:before | 前
:around | 前後

### 例
    define_model_callbacks :initializer, only: :after


### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/callbacks.rb#L109)
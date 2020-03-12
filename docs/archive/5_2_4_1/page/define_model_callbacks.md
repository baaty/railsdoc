---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/callbacks.rb#L108)
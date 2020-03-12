---
layout: archive_page
---
### 説明
複製可能か？

### 使い方
    duplicable?

### 例
#### 複製可能
    "hoge".duplicable?
    # true

#### 空文字の場合
    "".duplicable?
    # true

#### 複製不可能
    method(:puts).unbind.duplicable?
    # false

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/object/duplicable.rb#L113)
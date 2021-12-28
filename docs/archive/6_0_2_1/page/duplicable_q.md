---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/object/duplicable.rb#L36)
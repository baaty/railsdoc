---
layout: page
---

### 説明

複製可能か

### 使い方

    duplicable?()

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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/object/duplicable.rb#L36)

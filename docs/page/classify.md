---
layout: page
---
### 説明
テーブル名からモデル名へ変換  
「config/initializers/inflections.rb」に定義を追加することによって可能

### 使い方
    classify(テーブル名)

### 例
#### 「people」を変換
    classify("people")
    # "Person"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L215)
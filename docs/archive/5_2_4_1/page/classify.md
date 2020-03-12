---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/inflector/methods.rb#L201)
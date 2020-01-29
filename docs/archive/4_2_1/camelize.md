---
layout: page
---
### 説明
ファイル名からクラス名へ変換
「config/initializers/inflections.rb」に定義を追加することによって可能

### 使い方
    <ファイル名>.camelize

### 例
##### 「product」を変換
    "product".camelize
    # "Product"

#### 「backoffice/session」を変換
    "backoffice/session".camelize
    # "Backoffice::Session"